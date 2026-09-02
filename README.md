# FlowImageMaster — 다운로드

Google Flow에서 장면 이미지를 대량 생성하고, 장면마다 한 장을 고르고, 업스케일까지 처리하는 데스크톱 앱입니다. 이 저장소는 **배포용**입니다. 소스 코드는 별도 비공개 저장소에 있습니다.

최신 버전: [Releases](https://github.com/ohmyzhs/flow-image-master-releases/releases/latest)

## Windows

| 파일 | 설명 |
|---|---|
| `FlowImageMaster-windows-x64-portable.exe` | 설치 없이 실행되는 단일 파일. 원하는 폴더에 두고 더블클릭 |
| `FlowImageMaster_<버전>_x64-setup.exe` | 설치 프로그램. 시작 메뉴·제거 항목이 생기고, WebView2 런타임이 없는 PC에서는 자동으로 받아 설치 |

처음 실행하면 **"Windows의 PC 보호"** 파란 창이 뜹니다. 코드 서명이 없어서 나오는 SmartScreen 경고이며 한 번만 뜹니다. **추가 정보 → 실행**을 누르면 됩니다.

필요한 것:

- **Google Chrome 또는 Microsoft Edge.** Chrome을 먼저 찾고, 없으면 Edge를 씁니다. Edge는 Windows에 기본 포함이라 따로 설치할 것이 없습니다. 앱은 사용자의 브라우저 프로필을 건드리지 않고 전용 프로필을 만듭니다.
- **WebView2 런타임.** Windows 10/11에는 이미 있습니다. 포터블 exe가 창을 못 띄우면 설치 프로그램을 쓰세요.
- **Vulkan을 지원하는 GPU 드라이버.** 업스케일에만 필요합니다. 없으면 생성과 선택은 되고 업스케일만 실패합니다.

## macOS

`FlowImageMaster_<버전>_aarch64.dmg` (Apple Silicon). 서명이 없어 최초 실행 시 **시스템 설정 → 개인정보 보호 및 보안 → "확인 없이 열기"**를 한 번 눌러야 합니다. Google Chrome이 설치되어 있어야 합니다.

## 사용법

앱을 실행하고 `*_flow_prompts.txt` 파일을 창에 드롭하면 프로젝트가 등록됩니다. [Google 로그인]으로 Flow 계정에 한 번 로그인한 뒤 [생성 시작]을 누르면 캐릭터 → 장면 순으로 생성되고, 끝나면 장면마다 후보 중 한 장을 고르는 화면으로 이어집니다. 실행 중에는 화면 꺼짐·잠금이 자동으로 억제됩니다.
