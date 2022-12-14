## 1.1.10 MVVM 패턴

![스크린샷 2022-10-19 오후 9 47 49](https://user-images.githubusercontent.com/74235102/197384225-75079021-3417-46ad-b1f2-673570d1c961.png)

이 그림에서의 뷰모델은 뷰를 더 추상화한 계층.

MVVM은 MVC와 다르게 커맨드와 데이터 바인딩을 가지는 것이 특징

뷰와 뷰모델 사이에 양방향 데이터 바인딩을 지원하고 UI를 별도의 코드 수정 없이 재사용할 수 있고 단위 테스트하기 쉽다는 장점이 있다.

MVVM패턴 예 : 뷰

MVVM 패턴을 가진 대표적 프레임워크로 뷰가 있다.

Vue.js 는 반응형이 특징인 프레임워크이다.

함수를 사용하지 않고 값 대입만으로도 변수가 변경되며 양방향 바인딩, html을 토대로 컴포넌트를 구축할 수 있다.

### View

사용자가 직접 보는 화면 UI로 보면 된다.

화면에 무엇을 그릴지 결정하고, 사용자와 직접적으로 상호작용하는 부분으로 데이터의 변화를 감지하기 위한 옵저버를 가지고 있다.

### ViewModel

UI를 위한 데이터를 가지고 있음.

View와 분리된 구조를 가지기 때문에 View의 생명주기에 영향을 받지 않는다.

View와 Model간의 데이터 처리/중개를 담당

### Model

애플리케이션에 사용되는 데이터 및 데이터 조작부분을 담당

axios를 사용해서 데이터를 받아오면 이부분이 아닐까 싶은..

### 동작 순서

1. 사용자의 Action들이 View를 통해 들어온다.
2. View에 Action이 들어오면, Command 패턴으로 ViewModel에 Action을 전달한다.
3. ViewModel은 Model에게 데이터를 요청한다.
4. Model은 ViewModel에게 요청받은 데이터를 응답한다.
5. ViewModel은 응답 받은 데이터를 가공하여 저장한다.
6. View는 ViewModel과 데이터 바인딩을 하여 화면에 나타낸다.

### 왜 쓰는가?

UI와 로직의 분리

화면에 보여지는 UI와 실 데이터를 처리하는 로직을 분리하여 유지보수 및 개발 효율을 높일 수 있음.
