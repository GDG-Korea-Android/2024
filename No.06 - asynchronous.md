## 6. <보기>는 안드로이드 개발에 활용되는 비동기 처리방식에 대한 설명이다. <보기>에서 설명하는 비동기 처리방식은?
### <보기>
- This class was deprecated in API level 30.
- Use the standard java.util.concurrent or Kotlin concurrency utilities instead.

### ⓵ Java Threads
- Java에서 기본적으로 제공하는 스레드 기반의 비동기 처리 방식입니다.
- 멀티스레딩을 구현하기 위해 java.lang.Thread 클래스를 사용하거나, Runnable 인터페이스를 구현하여 스레드를 생성할 수 있습니다.
- 개발자가 직접 스레드를 생성하고, 시작(start), 종료(join), 상태 확인 등의 작업을 관리해야 합니다.
- 멀티스레드 환경에서 동기화 작업(synchronized)이 필요할 수 있습니다.

### ⓶ AsyncTask
- Android에서 비동기 작업을 처리하기 위해 제공되던 클래스입니다.
- 백그라운드 작업과 UI 업데이트를 간단히 처리할 수 있지만, API 30부터 Deprecated되었습니다.
- Activity나 Fragment의 생명주기와 동기화되지 않아, 메모리 누수 및 잘못된 UI 업데이트를 유발할 수 있습니다.
- 유지보수가 어렵고, 성능 최적화에도 제한이 있습니다.

### ⓷ RxJava
- ReactiveX 기반의 비동기 처리 라이브러리로, 데이터 스트림과 이벤트 기반 비동기 처리를 지원합니다.
- 콜백 지옥 문제를 해결하고, 복잡한 비동기 로직을 간결하게 표현할 수 있습니다.
- 고급 사용 사례에 적합하지만, 학습 곡선이 높고, 과도하게 사용하면 코드 복잡도가 증가할 수 있습니다.
  
### ⓸ Kotlin Coroutines
- Kotlin에서 기본적으로 제공하는 경량 스레드 기반의 비동기 처리 방식입니다.
- 비동기 코드를 동기적으로 작성할 수 있어 가독성이 높으며, 유지보수성이 뛰어납니다.
- launch, async와 같은 코루틴 빌더를 활용하여 백그라운드 작업을 효율적으로 관리할 수 있습니다.
- Android Jetpack 라이브러리와의 강력한 통합으로, UI와 백그라운드 작업 간의 안전한 동기화가 가능합니다.

### ⓹ WorkManager
- Android Jetpack 라이브러리로, 장기 실행 작업 및 지연된 작업을 관리할 수 있습니다.
- 네트워크 상태, 배터리 상태, 기기 조건 등을 기반으로 작업을 예약할 수 있으며, 주로 데이터 동기화나 주기적 작업에 사용됩니다.
- 비동기 작업을 체계적으로 처리하며, 앱이 종료되어도 작업이 유지됩니다.

### 결론
- <보기>에서 언급된 클래스는 AsyncTask를 의미합니다.
- API 30부터 Deprecated되었으며, Kotlin Coroutines 또는 java.util.concurrent 기반 유틸리티를 사용하는 것이 권장됩니다.
