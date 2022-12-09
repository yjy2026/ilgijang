# Chain-of-Thought Prompting Elicits Reasoning in Large Language models

## Introduction

1. LLM 이 NLP 잘해줌.
    - scale 만 키우면 엥간한 건 해결됨 ㅋㅋ
    - 근데 arithmetic, commonsense, symbolic reasoning 은 scale 만 키운다고 해결되지 않는 것 같음;;
2. "간단한 method" 로 LLM 의 reasoning 능력을 잠금해제할 수 있는지 알아보자.
    - arithmetic reasoning 은 최종 정답을 도출하는 __근거__(과정)를 생성할 수 있을 때 잘 된다.
        - 근데 그 근거라는 걸 large set 으로 만드는 것 자체가 또 골치아픔.
        - 그냥 간단하게 input-output 예시 던져주는게 덜 복잡함. 
    - LLM 은 prompting 이라고 하는 예시 몇개 던져주면 알아서 zero-shot, few-shot 으로 잘 하는 능력을 갖고 있다.
        - 근데 reasoning 만 하려고 하면 헛소리함.
        - 모델 scale 키워도 prompting 이 성능면에서 향상된다거나 하는 감흥이 딱히 없음.
3. 위 두 아이디어의 장점을 잘 조합해서, 각각의 한계를 극복해보자.
    - reasoning 을 위해 <input, chain of thought, output> 을 prompt 로 활용하는, __chain-of-thought prompting__ 기법에 대해 알아보자!
4. chain-of-thought prompting 이 그냥 기존 prompting 에 비해 얼마나 좋은지 실험해보기로 했어요.
    - arithmetic, commonsense, symbolic reasoning benchmarks 등의 종목에서 비교해볼거예요.
    - 
