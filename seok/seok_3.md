+ ## 9장 컨테이너와 문자열
+ Container라고 플러터에 있는데 반갑다.
+ 배열로 저장할 때 값 삽입 시 복사가 필요
+ 하지만 연결리스트는 삽입 시 계산량이 O(1)이다.
+ 하지만 순서 탐색 시 배열이 유리하다.
+ 사전, 해시, 트리 중 오더가 가장 작은 '해시 테이블'
+ 하지만 낭비되는 공간 많다. - 이렇듯 다 장단이 있음
+ ### 만능 컨테이너란 없다
+ 최적의 컨테이너를 찾는 것이 좋다.
+ c언어가 오류를 출력하는 것을 보니 c언어를 배울 때가 새록새록..
+ 세상은 프로그래머에 의해 돌아가고 있지 않으며, 
+ 구현에 의존하지 않는 다른 방법도 있다는 것을 기억해야

+ ## 10장 병행 처리
+ ### 병행처리란 잘게 분할해서 실행해 사용자가 동시에 처리되는 것처럼 보이는 것
+ 운영체제시간에 배운 것들이 나오는데
+ Race condition 경합 상태 : 한 프로그램이 쓰다가 다른 프로그램이 뺏는 것
  + 경합 상태의 3조건
  + 2가지 처리가 변수 공유
  + 적어도 하나의 처리가 그 변수 변경
  + 한쪽 처리가 한 단락 마무리 되기 전에, 다른 한 쪽의 처리가 끼어들 가능성 있음
+ 이 3가지 중 하나만 불만족하면 경합 상태는 일어나지 않는다.
+ 공유하지 않는다.
  + 유닉스 체제에선
    + 사용해도 좋은 메모리 영역을 결정, 다른 프로세스와 메모리를 공유하지 않는다.
+ 액터
  + 메모리를 공유한다가 아닌 메시지를 보낸다.
+ 변경하지 않는다.
  + 3조건 중 두번째 조건을 안하는 것.
  + const 나 val 로 선언
  + 읽기 위해 getter를 만들지만 setter를 만들지 않는 것
+ 끼어들지 않는다.
  + 3번째 조건을 안하는 것.
  + 협력적 스레드
  + 락, 세마포 - 운영체제 시간에 배운 것
    + 락의 문제점 - 데드락 : 모든 프로세스가 끼어들지 말라고 하는 것
    + 어중간한 상태 : 트랜잭션 상태