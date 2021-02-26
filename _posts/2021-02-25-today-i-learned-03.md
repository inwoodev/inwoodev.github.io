---
layout: post
title:  "Feb 25, 2021, TIL (Today I Learned) "
summary: "iOS 커리어 스타터 캠프 2기"
author: inwoodev
date: '2021-02-25 22:35:23 +0530'
category: SwiftProgramming
thumbnail: /assets/img/posts/light-bulbs.jpg
keywords: computerscience, cs, ios, swift, api, design, guideline, programming, startercamp, day3
permalink: /blog/TIL(Today I Learned)/
usemathjax: true

---

### 수업 학습내용

---

#### **CS 공부 1일차**

#### 주기억장치 vs 보조기억장치

##### 주기억 장치

**<특징>**

1. ROM

   - `Read Only Memory`
   - `비교적 느림`

   - `항구적 기억장치`
   - `비 휘발성 메모리`

2. RAM

   - `Random Access Memory`

   - `비교적 빠름`

   - `휘발성 메모리`, `비교적 빠른 속도`, 

     ex): 주기적으로 재충전이 필요한 `DRAM`(동적 램)

     Ex): 전원이 유지되는 상태에서 기억 내용이 유지되는 `SRAM`(정적 램)



##### 보조기억 장치

**<특징>**

\- 중앙처리장치와 직접 자료 교환이 **불가**

\- 접근시간이 비교적 오래 걸림

\- 일반적으로 주기억장치에 데이터를 저장할 때는 **DMA** 방식을 사용

\- CPU가 직접 접근 불가



**<보조기억장치 종류>**

- 하드디스크 ( 읽기 쓰기를 하는 컴퓨터 외부 기억장치)
- CD (디지털 기억 매체)
- 자기 테이프 (플라스틱 자기 테이프를 사용한 대용량 디지털 기억 장치)
- 광디스크:  대용량 기억장치 & 빛 반사를 이용해서 자료 읽어내는 저장매체



*참고: [주기억장치와 보조기억장치의 종류와 특성 :: 틍하의 블로그 (tistory.com)*](https://kshman94.tistory.com/111)



### 프로젝트 진행 중 학습 내용

---

#### API Design GuideLine (지속적인 업데이트 예정)

##### `직관적인 변수명` (Naming)

- 애매모호한 단어 지양

  - 확실한 뜻 전달을 위해 특정 메소드의 자세한기능을 서술하자

  ex): `intArray.removeAllData() // good`

  ex): `intArr.remove() // bad. remove what?`

- 불필요한 단어 생략

##### `문법 지향적 메소드 표현`

- 마치 영어 문서를 읽는 느낌을 형성 해 보자.

  ex):

  ```
  x.insert(y, at: z)          “x, insert y at z”            // good
  x.subViews(havingColor: y)  “x's subviews having color y” // good
  x.capitalizingNouns()       “x, capitalizing nouns”       // good
  ```

  ```
  x.insert(y, position: z) // weird
  x.subViews(color: y)     // weird
  x.nounCapitalize()       // weird
  ```

  *출처: [Swift.org - API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)*

- `make`를 사용하여 팩토리 메소드 이름

  ex: `makeIterator()`

- 부작용 유무에 따른 메소드 이름 지정

  * 부작용이 없는 메소드 → 명사구로 생성 ex: `home.distance(to: y)`
  * 부작용이 있는 메소드 → 동사구로 생성 ex: `print()`, `array.append(number)`



#### 다음 수업준비:

##### 스위프트 옵셔널(Optional)

옵셔널이란...값이 `있을 수도` `없을 수도 있음`을 나타내는 표현이다.

	- 변수나 상수에 값이 있다는 것을 보장할 수 없다.
	- 그러니 nil일 수도 있으니 사용에 주의하라라고 받아들일 수 있다.

*`nil`은 옵셔널이 선언된 곳에만 사용할 수 있다.



###### 옵셔널 바인딩

```swift
var myName: String? = "james"
if let name = myName {
	print("My name is \(name)")
} else {
  print("my name is nobody")
}
```

- if 구문 실행하는 블록 안쪽에서만 `name` 임시 상수를 사용할 수 있다. 해당 블록 밖 그리고 else 블록에서도 사용이 불가하다. 
- `쉼표(,)`를 사용해서 바인딩할 옵셔널을 나열하면 여러 옵셔널 값을 추출할 수 있다. 단 옵셔널 중 하나라도 값이 없으면 해당 블록 내부의 명령어는 실행 되지 않는다.

### 문제점 / 고민한 점

---

- while 문 안에서 함수를 재귀함수 형식으로 호출할 때 while 조건이 반영되지 않았던것 같다. 그 때문에 호출할 때 알 수 없는 오류가 생성되었고 이 때문에 꽤나 고생하였다. 분명 배열안에 3 개의 정수가 들어있어야 하는데 확인 해 보니 갑자기 정수가 없어지고 index오류가 발생하는 이해할 수 없는 상황을 격었다. 해당 부분을 해결하려 2시간동안 Fezz와 고민하였다. Fezz 덕분에 풀 수 있었다. 역시 코딩마스터...

- 최대한 기능을 잘게 나누어서 메소드화 하려고 노력하였다. 또한 이해하기 어려운 코드에 주석을 달아보았다. 나중에 다른 사람 또는 기억을 못하는 미래의 나 자신이 해당 기능을 다시 봤을 때 어떻게 동작하는지 다시 생각 해 내기를 바라며 주석을 달았다.
- API Design Guide를 참고하여 코드를 작성하려고 노력하였다. 문법 지향적으로 작성해야 한다는 것을 배웠다.



### 해결 방법

---

while 문 안에서 함수를 재귀함수 호출하기 보다는 해당 함수를 다른 형식으로 변경을 해 보았다. 재귀함수가 아니라 bool 값을 return하는 함수로 구현 한 뒤 while 문 안에서 

```swift
 while gameCount > 0 {
            printInstruction()
            var inputNumber = readLine()!.split(separator: " ").map { Int(String($0)) ?? -1 }
            if !checkInput(userInput: inputNumber) {
                continue
            }
```

```swift
func checkInput(userInput: [Int]) -> Bool {
        if userInput.count == 3 && !userInput.contains(-1) {
            return true
        }
        else {
            printError()
            return false
        }
    }
```

해당 방법을 구현할 때 `dump`메소드가 매우 큰 역할을 하였다. 배열 값의 변화를 실시간으로 볼 수 있었기에 문제의 원인을 대략적으로나마 파악할 수 있었다. 앞으로도 dump 자주 써야겠다.

