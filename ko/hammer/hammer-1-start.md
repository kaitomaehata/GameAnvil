## Game > GameAnvil > 테스트 개발 가이드 > 시작하기

## GameHammer

GameHammer는 GameAnvil 엔진을 이용한 게임 서버 개발 도구로 강력하고 편리한 테스트 도구입니다. 실제 커넥터에서 제공하는 모든 기능을 사용할 수 있으며, 다양한 테스트 케이스를 만들 수 있는 API를 제공하고 있습니다. 또한, 스트레스 테스트를 위해 다수의 GameHammer를 동시에 실행하고, 그 결과를 취합해 바로 확인할 수 있습니다.

### 시스템 요구 사항

GameHammer를 사용하려면 다음과 같은 사항이 필요합니다. 

- 지원하는 언어
    - Java
- 타깃 개발 환경
    - IntelliJ
- 지원하는 네트워크 프로토콜
    - TCP/IP
    - SSL over TCP/IP
- 사용 가능한 응용 프로토콜 형식
    - Google Protocol Buffers
    - Google FlatBuffers(예정)
    - 커스텀 바이트 스트림
    - HTTP/HTTPS(특정한 용도로 한정)

### 특장점

GameHammer는 다음과 같은 기능을 지원합니다.

- 커넥터와 대응하는 모든 기능 지원
- Sync/Async 방식 모두 지원
    - Async 방식의 API 제공
    - Sync 방식을 위한 future 제공
- 수천 개 또는 그 이상의 커넥션 동시에 사용 가능
- 상태 기반의 시나리오 관리 기능 지원

### 레퍼런스 프로젝트

| 서버                                                         | 테스트 코드                                                  | 설명                                             |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ |
| [sample-game-server](https://github.com/nhn/gameanvil.sample-game-server.git) | [sample-game-test](https://github.com/nhn/gameanvil.sample-game-test.git) | 실제 게임 서버와 GameHammer를 사용한 테스트 코드 |

## 프로젝트에 GameHammer 추가하기

GameHammer는 GameAnvil과 마찬가지로 Maven을 통해 배포됩니다. pom.xml 파일의 dependencies 요소에 다음과 같이 추가하면 GameHammer를 사용할 수 있습니다.

```
...
<dependencies>
        ...
        <!-- GameHammer -->
        <dependency>
			<groupId>com.nhn.gameanvil</groupId>
			<artifactId>gamehammer</artifactId>
			<version>1.4.1-jdk11</version>
		</dependency>
        ...
<dependencies>
...        
```

## Maven으로 GameHammer jar 파일 생성하기

GameHammer를 이용해 테스트 시나리오를 작성한 뒤 GameAnvil 콘솔에서 테스트할 목적 등으로 jar 파일을 생성할 수 있습니다. 여기에서는 메이븐을 통해 업로드용 jar 파일을 생성합니다.

GameHammer를 추가한 프로젝트의 pom.xml이 있는 디렉터리에서 아래 명령어를 실행합니다.

```
mvn package
```

명령어 실행 후, 빌드 과정이 출력되고 마지막으로 빌드에 성공했다는 메시지를 확인합니다. 아래와 같이 나오면 성공입니다.

```
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  7.880 s
[INFO] Finished at: 2023-11-13T17:49:48+09:00
[INFO] ------------------------------------------------------------------------
Process finished with exit code 0
```

새롭게 생성된 타깃 디렉터리 안에서 빌드된 파일을 확인할 수 있습니다.
