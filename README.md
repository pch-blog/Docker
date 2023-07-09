# Docker

- Language : GO (Google)

Docker는 컨테이너 기술을 사용하여 소프트웨어 개발 및 배포를 단순화하는 도구로 컨테이너는 코드와 해당 코드를 실행하는 데 필요한 종속성 및 도구가 포함된 소프트웨어 패키지입니다. Docker를 사용하면 동일한 코드와 도구를 포함하는 컨테이너를 만들 수 있으며, 이는 Docker가 활성화된 모든 환경에서 동일한 결과를 생성하는 장점이 있습니다.

Docker를 사용하면 개발자는 소프트웨어 개발 및 배포를 위한 표준화된 환경을 구축할 수 있습니다. 이를 통해 개발자는 코드가 항상 올바른 환경에서 실행되도록 보장 가능하며 모든 OS환경에서 실행되므로 개발자는 각자의 상황에 맞는 환경에서 개발하고 테스트할 수 있습니다.

또한 컨테이너의 생성 및 관리를 단순화하는 도구입니다. 이를 통해 개발자는 응용 프로그램을 배포할 때 독립적이고 표준화된 응용 프로그램 패키지가 필요합니다. Docker를 사용하면 프로그래밍 언어를 Docker 컨테이너에 고정하여 코드가 항상 올바른 언어 버전에서 실행되도록 할 수 있습니다.

## Docker를 사용하는 방법

1. Docker 설치
   - Docker는 Windows, macOS, Linux 등 다양한 운영체제에서 사용 가능
   - 각 운영체제에 맞는 Docker 설치 방법을 찾아 설치
2. Dockerfile 작성
   - Dockerfile은 Docker 이미지를 만드는 데 사용되는 스크립트
   - Dockerfile을 작성하여 Docker 이미지 생성
3. Docker 이미지 빌드
   - Dockerfile을 사용하여 Docker 이미지를 빌드
4. Docker 컨테이너 실행
   - Docker 이미지를 사용하여 Docker 컨테이너를 실행

## Docker를 사용하여 개발 및 배포하는 방법
Docker를 사용하면 개발자는 동일한 환경에서 어플리케이션을 실행할 수 있으며, 이는 응용 프로그램을 배포할 때 매우 중요한 재현성을 보장합니다. 또한, Docker는 컨테이너 기술을 사용하여 소프트웨어 개발 및 배포를 단순화하는 도구입니다.

1. 개발
   - Docker를 사용하여 개발하면 동일한 환경에서 어플리케이션을 실행 가능
   - 동일한 환경에서 어플리케이션을 실행 가능한 것은 응용 프로그램을 배포할 때 매우 중요한 재현성을 보장
2. 테스트
   - Docker를 사용하여 테스트하면 응용 프로그램을 실행하는 데 필요한 모든 종속성을 포함하는 컨테이너 생성 가능
   - 응용 프로그램을 실행하는 데 필요한 모든 것이 포함된 환경을 보장 가능 
3. 배포
   - Docker를 사용하여 배포하면 응용 프로그램을 배포하는 데 필요한 모든 것을 포함하는 컨테이너를 생성 가능
   - 응용 프로그램을 배포하는 데 필요한 모든 것이 포함된 환경을 보장 가능

# Problem Solution : Docker
소프트웨어 개발에서 독립적으로 표준화된 어플리케이션 패키지를 원하는 이유에 대해 알아야 합니다. 각각의 다른 개발 환경에서 개발하며 어떤 최신버전의 언어와 도구를 사용하여 성공적으로 실행되는 경우 이전에 버전에서는 실행할 수 없는 문법이나 기능이 있을 것입니다. 하지만 최신버전이 로컬 개발환경에만 적용되어 있을 경우 많은 문제가 발생 할 수 있습니다. 이런 문제를 해결하기 위해 개발환경과 동일한 환경을 갖는데에 매우 큰 의미가 있습니다.

또한, 한 팀 내에 속해 있어 동일한 프로젝트를 수행하는 경우, 각각의 다른 버전의 사용하고 있을 수 있습니다. 이때 서로 코드를 공유하면 하위 버전을 사용하는 사람들에게는 작동하지 않을 수 있습니다. 하위 버전을 사용하느 사람들이 최신 버전으로 업데이트 하는 것은 문제가 되지 않으며. 시스템에서 쉽게 업데이트를 할 수 있다는 것입니다.

또한, 혼자 작업하는 프로젝트가 여러 개일 경우 충돌하는 버전이 있을 수 있습니다. 어떤 프로젝트에서 어떤 이유로든 각 프로젝트마다 다른 버전의 언어를 사용하고 있을 수 있습니다. 이럴 경우 프로젝트 A에서 프로젝트 B로 전환할 때마다 잘못된 버전을 제거하고 올바른 버전을 설치해야 한다는 문제가 발생합니다. 이런 문제들을 해결하는데 컨테이너 작업을 고려해야하고 도커가 컨테이너에 매우 유용한 도구인 것입니다.

따라서, 도커를 사용하여 각각의 프로젝트에 그들만의 컨테이너가 존재하도록 도와줌으로써, 프로젝트를 전환하는 경우 버전의 업그레이드 혹은 다운그레이드가 필요할 때마다 매번 제거하고, 다시 설치할 필요 없이 다른 컨테이너를 시작하는 것으로 쉽게 프로젝트를 전환할 수 있습니다.