## 기능 구현 목록

### MVP 기능 흐름

1. 다리 생성하기

2. 건널 수 있는 칸 생성하기

3. 플레이어가 이동할 칸 선택하기

4. 잘못된 칸을 밟았을 때 재시작할지 종료할지 선택하기

5. 게임이 끝나고 최종 값 출력

## 기능 구현 목록

### 1. 다리 생성하기

#### 예외처리

- [x] 3~20 사이의 숫자 입력값 이외 전부 예외처리

#### 기능구현

- [x] 입력받은 숫자 만큼의 다리 길이 생성
- [x] BridgeMaker 객체 의도에 맞게 다리 생성
- [x] 다리의 시작은 [, 끝은 ], 구분은 | 문자열로 구분하여 출력

### 2. 건널 수 있는 칸 생성하기

#### 기능구현

- [x] 0과 1의 무작위 값을 이용해 건널 수 있는 칸 설정
- [x] 0일 경우 아래칸, 1인 경우 위 칸이 건널 수 있는 칸

### 3. 플레이어가 이동할 칸 선택하기

#### 예외처리

- [x] 대문자 U,D 이외 전부 예외처리

#### 기능구현

- [x] 대문자 U를 입력받으면 위 칸, D는 아래 칸 이동하기
- [x] 이동한 칸을 건널 수 있다면 O, 없다면 X로 표시하기

### 4. 잘못된 칸을 밟았을 때

#### 예외처리

- [x] 대문자 R, Q 이외 전부 예외처리

### 기능구현

- [x] 대문자 R을 입력 받았으면 재시작, Q를 받았으면 종료하기

### 5. 재시작했을 경우

#### 기능구현

- [x] 처음에 썻던 다리 재사용

### 6. 게임이 종료됐을 경우

#### 기능구현

- [x] 다리를 다 건너서 게임이 종료됐으면 성공, Q를 눌러서 종료됐으면 실패 출력하기
- [x] 총 시도한 횟수 출력하기

### 7. 예외처리 규칙

- [x] throw문 을 사용해 에러 문구를 출력한 후 그 부분부터 다시 입력 받기

### 추가 과제 목표

- [x] MVC 패턴으로 클래스 관리
- [x] 추상 클래스나 인터페이스를 사용 용도에 맞게 구현하여 객체지향 프로그래밍 시도하기
- [x] 의존성 주입을 통해 클래스들간의 의존성 느슨하게 하기
![슬라이드2](https://user-images.githubusercontent.com/82035356/203296201-e8948f28-4ef5-4b82-b95c-2a2060a76f16.JPG)
![슬라이드3](https://user-images.githubusercontent.com/82035356/203296215-c0e1cdbd-b6e6-4a75-b87f-a8d627d6b9ce.JPG)

- [x] 인터페이스와 추상 클래스를 상황에 맞게 판단하여 MVC 패턴에 맞게 구성했다.
### 도메인 분리

![domain_bridge](https://user-images.githubusercontent.com/82035356/202850717-e3e52815-0d5a-4120-a8c8-d6ac6674d9c5.jpg)

서비스 흐름에 따라 도메인을 분리하고, 비즈니스 로직과 UI 로직을 구분.
비즈니스 로직에 해당하는 11가지의 테스트 진행 예정

### 테스트 목록

- [x] 사용자가 3과 20사이 숫자로 다리 길이를 입력했는지 확인했다.
- [x] 0과 1의 무작위 값으로 건널 수 있는 칸과 없는 칸을 생성했다.
- [x] 입력 받은 다리 길이로 다리를 생성했다.

---

- [x] 사용자가 대문자 U나 D를 입력했는지 확인했다.
- [x] U를 입력 받으면 위 칸, D를 입력 받으면 아래 칸으로 건넜는지 확인했다.
- [x] 다리 칸마다 생성된 무작위 숫자를 통해 건널 수 있는 지 없는 지 판단했다.

---

- [x] 사용자가 대문자 R이나 Q를 입력했는지 확인했다.
- [x] R을 입력 받았으면 다시 시작하고, Q를 입력 받았으면 종료한다.

---

- [x] 처음 생성된 다리를 재사용했다.

---

- [x] 다리를 다 건너서 게임이 끝난 경우 성공, 아닌 경우 실패로 처리했다.
- [x] 총 시도한 횟수를 계산했다.
