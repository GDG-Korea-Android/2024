# 문제 - Kotlin
## 1. 다음 중 Kotlin에 대해 잘못된 설명은?
### ⓵ Java와 완벽하게 호환되며, 기존 Java 코드를 그대로 사용할 수 있다.
- Kotlin은 Java와 동일한 JVM에서 실행되며, 컴파일된 바이트코드의 구조가 Java의 바이트코드와 동일하며, 100% 상호 운용성을 보장하도록 설계되었습니다.
### ⓶ 기본적으로 Null 안정성을 지원하며, NullPointerException 발생 가능성을 줄인다.
- Kotlin은 Nullable과 Non-Nullable 타입을 명시적으로 구분합니다.
- ?.(safe call), ?:(elvis 연산자), !!(Not Null 단언 연산자) 같은 연산자를 통해 Null 안정성을 제공합니다
### ⓷ 람다식과 고차함수를 지원하며, 컬렉션 작업이 간단하고 효율적이다.
- 람다식 : 람다식은 익명 함수의 간단한 표현으로, 코드 블록을 함수처럼 사용할 수 있습니다.
- 고차함수: 다른 함수를 파라미터로 받거나 반환값으로 함수를 반환하는 함수입니다.
- map, filter, forEach 등 람다함수와 고차함수를 활용하여 컬렉션 작업을 간결하고 효율적으로 처리할 수 있습니다.
### ⓸ Java의 클래스보다 경량화된 Data Class를 제공하며, 간단한 코드로 데이터를 표현할 수 있다.
- kotlin의 Data class는 데이터를 저장하고 관리하는데 최적화된 클래스 입니다.
- Data Class는 반드시 최소 하나의 속성을 기본 생성자에 선언해야 합니다.
- 데이터를 다루기 위한 표준 메서드(toString, equals, hashCode, copy)를 자동으로 생성합니다.
### ⓹ Kotlin은 Android에 최적화되어 있으며, Kotlin으로 작성된 코드는 Android 플랫폼 외에선 실행되지 않는다.
- Kotlin은 Android에 최적화되어 있지만, Android 전용 언어는 아닙니다.
- Kotlin의 범용성과 확장성 덕분에, Android 외에도 서버 개발, 웹 개발, iOS 개발, 멀티플랫폼 개발 등 다양한 환경에서 활용 가능합니다.

## 추가 개념 설명
### JVM
- JVM은 Java 프로그램을 OS에 종속되지 않고 실행하기 위한 가성 머신으로 Java 코드를 바이트 코드로 컴파일한 후 실행하는 역할을 합니다.
- Kotlin도 JVM에서 실행될 수 있도록 바이트코드로 컴파일되며, Java와의 상호 운용성을 제공합니다.
- 안드로이드는 전통적인 JVM을 사용하지 않습니다.
### Dalvik
- Dalvik Virtual Machine은 Android의 초기 런타임 환경으로, JVM과 유사하지만 Android 기기에 최적화된 가상 머신입니다.
- Android의 APK는 JVM 바이트코드가 아닌 DEX (Dalvik Executable) 형식으로 컴파일된 바이트코드를 포함하며, Dalvik에서 실행됩니다.
### ART (Android Runtime)
- ART는 Android 5.0(Lollipop)부터 도입된 런타임 환경으로, Dalvik을 대체하여 사용됩니다.
- Dalvik은 JIT 컴파일 기반의 런타임 환경이며 ART는 AOT 컴파일을 도입하여 Dalvik의 성능 문제(앱 실행 속도, 배터리 소모)가 개선되었습니다.
