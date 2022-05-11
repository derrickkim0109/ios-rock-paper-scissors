## iOS 커리어 스타터 캠프

### 묵찌빠 프로젝트 저장소

# [Step - 01]

# 🔽 FlowChart 
<img width="1012" alt="FlowChart" src="https://user-images.githubusercontent.com/59466342/163897965-b118205c-fac1-4f3e-b29b-c36fe27009db.png"> 

# 😄 프로젝트 수행 중 핵심 경험
- [x] Swift의 Optional 안전하게 처리하기
- [x] if와 switch 조건문의 차이와 장단점 비교해보기
- [x] 순환함수(재귀함수)와 반복문의 장단점 비교해보기
- [x] 함수가 한 가지 일만 하도록 기능 분리하기
- [x] guard 구문의 이해와 활용
- [x] Git의 커밋단위 고민하고 커밋에 적용하기
- [x] Git 커밋 로그 형식에 맞춰 커밋하기
- [x] 코딩 컨벤션 고민하기
- [x] 동료와 협업자세 고민하기
 
# 🔍 고민한 점
- if문과 switch 문의 차이점
> 제일 느낀 차이점은 if 문은 조건문에 쓰이는 프로퍼티를 자유롭게 조정할 수 있지만 switch문은 특정한 프로퍼티를 정해줘야 한다는 점입니다.
> 하기와 같은 이유로 조금 더 switch문을 사용 하였을때 직관적으로 코드를 볼 수 있다는 점도 생각 해보게 되었습니다.
> 또 다른 차이점이 있다면 어떤게 있을까요? **사파리의 생각이 궁금합니다**..ㅎㅎ

> switch내에 튜플을 사용하여 컴퓨터의 enum값과 사용자의 enum값을 지정하여 값을 비교 하는 부분을 만들었습니다. 

- enum 사용법 
> enum의 rawValue를 사용하기 위해 찾아본 결과 case의 첫번째 값에 0이라는 Int값을 주면 뒤에 이어지는 부분은 자동으로 숫자가 1씩 높은 값으로 적용 된다는 것을 알게 되었습니다. 하여 0 ~ 3까지의 값으로 ValueType을 지정하여 사용 하였습니다.

>또한 enum의 값에 해당하는 부분을 리턴 String 으로 사용하고자 value 프로퍼티를 enum extension내에 생성하여 Return 하도록 하였습니다.

- 함수 & 변수, 상수네이밍
> 이부분에서 상당히 애를 먹었는데요..! 컴퓨터의 임의의 패 생성을 위한 함수의 이름, 가위, 바위, 보의 enum 타입이름이 마음에 들지 않으나..
어떻게 바꿔주는게 좋을지 딱 떠오르지 않았습니다..(**조언이 많이 필요합니다**..ㅎㅎ)

- extension
> extension을 활용하여 String에서 사용 될 부분을 다른 디렉토리를 생성하여 빼는 작업을 해보았습니다. 확장성을 고려 하기 위해 String이 주체가 되는 부분들의 기능을 함수로 빼서 구현하는 방식을 시도 해보았습니다.

- 재귀함수 사용과 다른 반복문의 차이점
> 재귀함수를 run()함수에 적용 하여 사용해 보았습니다. 둘의 차이점에 대해서 검색해본 결과 맞는지 정확하지 않지만 재귀함수가 호출 될 때마다 스택은 새 로컬 변수와 매개 변수 집합을 저장하는 데 사용되고 반복문은 스택을 사용하지 않는다는 글을 읽었습니다. **해당 부분의 다른 부분이 있다면 어떤게 있을까요?** 

- Forced Unwrapping을 제외한 나머지 Optional 사용!
> 저번주에 배운 내용을 복습 하기 위해서 Optional Binding에서 부터 Optioanl Chaining, Nil-coalescing operator를 활용 하여 보았습니다!


# [Step - 02]
# 🔽 FlowChart
![Week 2 Step 2 Flowchart ](https://user-images.githubusercontent.com/59466342/164407385-24365b8a-af40-4ac4-ab81-74ae35384d16.jpg)

# 🔍 고민한 점
> while 문의 사용법, 네이밍, 특정 값을 enum화 

### While 문
> 저번주는 repeat while문, Step01 에서는 재귀함수를 경험해 보아서 while문을 사용해 보았습니다!

### Naming
> 최대한 자연스러운 네이밍을 만들어 보기 위해서 노력했으나.. 사파리가 보셨을때 어떠하신가요..?

### enum화
> user, computer String값이 고정되게 있어 enum화 시켜보았습니다. 

# 🙄 궁금한 점
> 처음에는 생성되는 값(묵,찌,빠)들과 해당 턴의 사용자(?)의 값을 struct로 뺄 생각으로 RockPaperScissors란 struct를 만들어서 그 안에 값들을 넣는 방식에 대해서 진행 했었습니다..

```swift
struct RockPaperScissors {
   let order: Player?
   let user: RockPaperScissorsType?
   let computer: RockPaperScissorsType? 

   init(order: Player? = .user , user: RockPaperScissorsType? = .none, computer: RockPaperScissorsType? = .none) {
       self.order = order
       self.user = user
       self.computer = computer
   }
}
```
> 이렇게 만들어서 진행하려고 하였었는데.. 잘 되지가 않았습니다.
인스턴스화 시켜 값은 들어오는데 값이 안 바뀌더라고요.. 머가 잘못 된걸까요?




