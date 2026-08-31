# Cobblemon Coop Distribution

코블몬 협동 서버의 클라이언트 자동 업데이트 배포 저장소입니다.

- `manifest.json`: alpha29 이하 설치기가 확인하는 기존 자체 모드 호환 목록
- `manifest-v2.json`: 고정 브리지가 확인하는 전체 모드·프로필·클라이언트 리소스 목록
- `files/`: 자체 제작 JAR, 브리지 관리 리소스와 고정 브리지 실행 파일
- 고정 브리지: [`cobblemon-coop-bridge.exe`](files/cobblemon-coop-bridge.exe)
- 공개 모드 의존성은 이 저장소에서 재배포하지 않고 공식 Modrinth CDN에서 받습니다.

고정 브리지를 한 번 설치한 뒤에는 일반 모드 추가·교체·제거, FancyMenu 설정·이미지, Minecraft/Fabric 프로필 갱신을 `manifest-v2.json`으로 배포합니다. 새 EXE는 브리지 엔진 자체를 변경해야 할 때만 필요합니다.

이 저장소에는 계정 토큰, 서버 비밀번호, 비공개 소스 코드를 올리지 않습니다.
