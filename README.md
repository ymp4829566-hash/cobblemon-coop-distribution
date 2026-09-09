# Cobblemon Coop Distribution

코블몬 협동 서버의 클라이언트 자동 업데이트 배포 저장소입니다.

- `manifest.json`: alpha29 이하 설치기가 확인하는 기존 자체 모드 호환 목록
- `manifest-v2.json`: 고정 브리지가 확인하는 전체 모드·프로필·클라이언트 리소스 목록
- `files/`: 자체 제작 JAR, 브리지 관리 리소스와 고정 브리지 실행 파일
- 고정 브리지: [`cobblemon-coop-bridge.exe`](files/cobblemon-coop-bridge.exe)
- 고정 브리지 SHA-256: `99B609A7CF931E83164A8FEE097DFB62411A84D42E6F7373CFEA1BE2847DB71F`
- 공개 모드 의존성은 이 저장소에서 재배포하지 않고 공식 Modrinth CDN에서 받습니다.

고정 브리지를 한 번 설치한 뒤에는 일반 모드 추가·교체·제거, FancyMenu 설정·이미지, Minecraft/Fabric 프로필 갱신을 `manifest-v2.json`으로 배포합니다. 새 EXE는 브리지 엔진 자체를 변경해야 할 때만 필요합니다.

현재 자체 제작 모드 배포 버전:

- 코블몬 협동 전투 `0.1.0-alpha.31`
- 코블몬 전설 조우 `0.1.0-alpha.2`
- 코블몬 전설 포켓몬 제단 `0.1.0-alpha.15`
- 쌍둥이 성소 챕터 맵 `0.2.0-alpha.4`
- 협동 메뉴 BGM `1.0.0`
- 두더지 시네마 플레이어 `0.1.0-alpha.4`
- Streamer Shops `0.1.0-alpha.21`

스이쿤 조우 영상은 GitHub Release 자산으로, 스트리머 상점 음성팩은 클라이언트 리소스팩으로 배포합니다.

`필드 6` 메뉴 BGM은 클라이언트 전용 `cobblemon-menu-bgm` 모드가 담당합니다. 마스터 채널 기준 30%로 반복 재생하고, 타이틀에서 설정·멀티플레이·접속 화면으로 이동해도 같은 인스턴스를 유지하며 월드 로드 시 정지합니다. 코옵 야생전 모드 JAR과 FancyMenu 레이아웃에는 메뉴 음악 코드나 음원이 포함되지 않습니다.

이 저장소에는 계정 토큰, 서버 비밀번호, 비공개 소스 코드를 올리지 않습니다.
