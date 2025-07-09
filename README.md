# miniRT

_ray tracing_

## 들어가기에 앞서

1. 본 저장소의 파일은 이미 make되어 있습니다.
2. 본 저장소의 모든 파일들 및 README는 WSL2 환경에서 실행될 것을 전제로 작성되었습니다.

**phong lighting model**을 구현하는 과제이다.

**miniRT** 실행 파일은 **환경광(ambient lighting), 카메라, 광원, 구체, 평면, 원기둥** 정보가 담겨 있는 .rt 파일을 파싱하여 3차원으로 렌더링할 수 있어야 한다. FdF의 wire frame 렌더링이 아닌, 보다 현실감 있는 3차원 렌더링으로 말이다.

`miniRT`를 실행하기 전 의존성 문제를 해결하기 위해 다음의 명령어를 실행해야한다.

```shell

sudo apt-get update && sudo apt-get install xorg libxext-dev zlib1g-dev libbsd-dev

```

아래와 같이 사용한다.

```shell

./miniRT rtFileName.rt

```

다음과 같은 보너스 항목을 구현하였다.

1. rt 파일의 첫번째 평면에 범프맵 텍스처 매핑
2. rt 파일의 첫번째 구에 체크 무늬 적용
3. 원뿔 도형을 렌더링할 수 있음

예제 rt 파일은 `maps` 경로에 위치한다.
