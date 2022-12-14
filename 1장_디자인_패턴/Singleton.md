## 싱글톤 패턴이란 ?
: 하나의 클래스에 오직 하나의 인스턴스만 가지는 패턴 (데이터베이스 연결 모듈에 많이 사용 !)

- 장점
: 다른 모듈들이 공유하면 사용하기 때문에 인스턴스를 생성할 때 드는 비용이 줄어든다.

- 단점 
: 의존성이 높아진다. 단위 테스트를 하기 어렵다.

### 의존성 주입 
: 싱글톤 패턴은 사용하기가 쉽고 굉장히 실용적이지만 모듈 간의 결합을 강하게 만들 수 있다는 단점이 있다.
이 때 의존성 주입(DI, Dependency Injection)을 통해 모듈간의 결합을 조금 더 느슨하게 만들어 해결할 수 있다.

- 장점
: 모듈들을 쉽게 교체할 수 있는 구조가 되어 테스팅하기 쉽고 마이그레이션하기도 수월하다. 또한, 구현할 때 추상화 레이어를 넣고 이를 기반으로 구현체를 넣어주기 때문에 애플리케이션 의존선 방향이 일관되고, 어플을 쉽게 추론할 수 있으면 모듈간의 관계들이 조금 더 명확해 진다.

- 단점
: 모듈들이 더욱 더 분리되므로 클래스 수가 늘어나 복잡성이 증가 될 수 있으면 약간의 런타임 페널티가 생기기도 한다.

- 의존성 주입 원칙
: "상위 모듈은 하위 모듈에서 어떠한 것도 가져오지 않아야 한다. 또한 둘 다 추상화에 의존해야 하며, 이때 추상화는 세부 사항에 의존하지 말아야 한다"
