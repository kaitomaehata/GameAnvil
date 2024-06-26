## Game > GameAnvil > 콘솔 사용 가이드 > Safe Pause

## Safe Pause란?

Safe Pause는 서비스 중지 없이 임의의 게임 노드를 일시 중단(Pause)할 수 있는 기능입니다. Safe Pause의 출발지 노드는 처리 중이던 모든 유저와 방 정보를 동일한 서비스를 수행 중인 도착지 노드로 실시간 전송(Transfer)합니다. 그러므로 동일한 서비스의 게임 노드가 2개 이상 존재하지 않는다면 Safe Pause를 사용할 수 없습니다.

Safe Pause 과정에서 전송을 보내는 쪽과 받는 쪽은 아래의 그림처럼 각각 **SAFE PAUSE** 상태와 **READY(LOCK)** 상태로 바뀝니다. **READY(LOCK)** 상태의 노드는 해당 Safe Pause 트랜잭션이 완료될 때까지 임의로 상태를 변경할 수 없습니다. 즉, 콘솔상에서 그 어떤 조작도 할 수 없습니다.

![그림](https://static.toastoven.net/prod_gameanvil/images/console/safe-pause/state.png)

Safe Pause가 완료되면 **Safe Pause** 상태는 **Pause** 상태로 바뀝니다. 당연히 해당 노드에는 그 어떤 유저나 방도 존재하지 않으므로 안전하게 셧다운할 수 있습니다. 패치나 점검이 필요하다면 이때 진행하면 됩니다. **Ready(Lock)** 상태 또한 Safe Pause가 완료됨과 동시에 **Ready** 상태로 전환되며 콘솔상에서 조작이 가능해집니다.

## Safe Pause 사용하기

운영 메뉴를 선택하면 Safe Pause 기본 화면을 볼 수 있습니다. 이 화면은 현재 진행 중인 Safe Pause와 관련된 노드 목록을 보여줍니다. **노드 선택**을 클릭하면 아래와 같이 Safe Pause를 수행할 노드를 선택하는 팝업이 열립니다.

![그림](https://static.toastoven.net/prod_gameanvil/images/console/safe-pause/node-selection.png)

Safe Pause의 **출발지 노드**와 **도착지 노드**를 각각 하나 이상 체크 박스를 클릭해 선택할 수 있습니다. 이때 처리 중인 유저와 방의 개수가 적은 노드를 **도착지 노드**로 선택하는 것이 유리합니다. 선택이 완료되었다면 **확인**을 눌러 Safe Pause를 **등록**합니다. 아직 수행 단계가 아닌 등록 단계임에 유의하십시오.

앞서 등록한 Safe Pause 관련 노드들은 다음과 같이 Safe Pause 기본 화면에 노출됩니다. 만약 잘못 등록한 노드가 있을 경우 목록 우측의 **-** 를 클릭해 삭제할 수 있습니다.

![그림](https://static.toastoven.net/prod_gameanvil/images/console/safe-pause/start.png)

모든 준비가 완료되었다면 **점검 실행**을 클릭해 Safe Pause를 시작할 수 있습니다. Safe Pause가 시작되면 다음과 같이 **서버** 메뉴에서 진행 중인 상태를 실시간으로 확인할 수 있습니다.

![그림](https://static.toastoven.net/prod_gameanvil/images/console/safe-pause/safe-pausing.png)

Safe Pause 과정을 통해 **출발지 노드**들의 유저와 방은 **도착지 노드**로 전송되며, 모든 과정이 완료된 뒤 **출발지 노드**들은 모두 자동으로 PAUSE 상태가 됩니다. 이제 PAUSE 된 노드들은 안전하게 종료할 수 있습니다.   

![그림](https://static.toastoven.net/prod_gameanvil/images/console/safe-pause/safe-pause-done.png)
