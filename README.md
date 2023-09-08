# 묵찌빠 프로젝트

## Step 1: 가위바위보 프로젝트

### 개요

command line tool 콘솔 프로그램

사용자에게 입력값을 받아 컴퓨터와의 가위바위보 게임을 진행하며 결과를 확인합니다.

### 팀원

![       Bello](https://prod-files-secure.s3.us-west-2.amazonaws.com/ffea4a1c-3b7d-4743-a030-3b14e2d929a0/74ebc407-5979-40ed-bdaf-49f495e1cfb5/image.png)

       Bello

![    Howard](https://prod-files-secure.s3.us-west-2.amazonaws.com/ffea4a1c-3b7d-4743-a030-3b14e2d929a0/19733376-ca36-40be-ba91-2979e5629c54/719695e0175e463db8ac992bc4fb98f7-sticker.png)

    Howard

## 프로젝트 구조

main.swift

- RPSGame 인스턴스를 생성하여 RPSGame의 `run()`를 실행시킵니다.

RPSGame.swift

- 프로그램을 실질적으로 동작시키는 `run()` 외에 기능을 구현하기 위한 함수가 정의되어 있습니다.
- `run()` : class내부에 run() 함수를 만고, 내부에 while 문을 통해서 사용자가 종료를 선택하거나, 특정 결과가 나오기 전까지 계속해서 루프를 돌도록 만듦.
- `getUserChoice()`, `generateRandomChoice()` : 사용자의 입력값을 받고, 컴퓨터의 가위바위보를 결정하는 메서드
- `generateRandomChoice(...)`, `generateRandomChoice(...)` : 사용자와 컴퓨터가 선택한 값을 비교하고 결과를 결정하여 출력하는 메서드

RPSModels.swift

- `enum Input` : 사용자의 입력을 케이스 별로 분류하여 처리합니다.
- `enum RPS` : 가위바위보의 케이스를 분류하고 비교합니다.

Printer.swift

- `enum Printer` : 게임을 진행하면서 출력되어야 하는 메시지들(게임 실행안내, 입력값 유효성체크, 승자 안내 등) 을 enum 타입으로 열거하여 코드 가독성을 높임

### 프로젝트를 통해 익히고 배운 **내용**

- Bello
    - guard문을 활용하여 옵셔널 바인딩 뿐만 아니라 여러 가지의 조건에 대한 처리에 대한 고민을 해보고 구현하며 경험을 얻을 수 있었습니다.
    - guard문의 else  {return} 의 경우, return을 해야한다는 관념에 사로잡혀 있었는데 continue 키워드를 이용하여 다음 주기의 반복문을 실행하는 방법을 깨달았습니다.
    - 열거형을 정의하여 케이스를 분류하고 각 케이스마다 처리하는 연습을 할 수 있었고, 코드의 반복을 피하기 위해서 노력을 해보았습니다.
    - 열거형의 Equatable, Comparable 프로토콜을 채택하여 값을 비교할 수 있다는 것을 알았으나 제대로 활용하기 위해서는 좀 더 공부해야 합니다.
- Howard
    - while 문의 활용법에 대해 알게 되었습니다. 만약 사용자의 입력값이 invalid 라면, while 문에서 이것을 받아 continue 키워드를 통해 다시 처음부터 동작 하도록 만들어서 굳이 재귀함수를 통해 반복적으로 함수호출을 안해도 되는 케이스를 경험했습니다.
    - 열거형 타입(enum)의 사용법에 대해 알게되었습니다. 아직은 케이스를 정의하여, 인스턴스에서 각 케이스가 할당되었을때 원하는 동작을 수행하는 기능정도밖에 모르지만, 조금더 학습하여 다양한 enum 사용법에 대해 알아볼 예정입니다.
    - 반복적인 동일 함수 사용을 피하고, 오타 입력에 대한 안정성을 enum 타입을 통해서 해결하는 방법을 배웠습니다.
    - Guard let 을 통해 optional 타입에 대해 유효성을 검증하는 방법을 배웠습니다.
    - Bello 와 협력해서 프로젝트 진행동안 많은 기본 문법의 사용방법이나 논리구조를 짜는 방식에 대해 배울 수 있었고, 서로 존중하며 프로젝트를 진행하는 경험을 한 것 같습니다.
