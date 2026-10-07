# Cobblemon Coop Distribution

코블몬 협동 서버의 클라이언트 자동 업데이트 배포 저장소입니다.

- `manifest.json`: alpha29 이하 설치기가 확인하는 기존 자체 모드 호환 목록
- `manifest-v2.json`: 고정 브리지가 확인하는 전체 모드·프로필·클라이언트 리소스 목록
- `manifest-neoforge-v2.json`: NeoForge 고정 브리지가 확인하는 별도 전체 목록
- `files/`: 자체 제작 JAR, 브리지 관리 리소스와 고정 브리지 실행 파일
- 고정 브리지: [`cobblemon-coop-bridge.exe`](files/cobblemon-coop-bridge.exe)
- 고정 브리지 SHA-256: `99B609A7CF931E83164A8FEE097DFB62411A84D42E6F7373CFEA1BE2847DB71F`
- NeoForge 고정 브리지: [`cobblemon-coop-neoforge-bridge.exe`](files/cobblemon-coop-neoforge-bridge.exe)
- NeoForge 고정 브리지 버전: `0.6.2-neoforge.ui1`
- NeoForge 고정 브리지 크기: `13,439,488 bytes` (13.44 MB, 20 MB 미만)
- NeoForge 고정 브리지 SHA-256: `6F211FD7653B09AB5B63BD5A0D2DA3F245A02FBB469952A686BA11A6591657D6`
- 공개 모드 의존성은 이 저장소에서 재배포하지 않고 공식 Modrinth CDN에서 받습니다.

고정 브리지를 한 번 설치한 뒤에는 일반 모드 추가·교체·제거, FancyMenu 설정·이미지, Minecraft/Fabric 프로필 갱신을 `manifest-v2.json`으로 배포합니다. 새 EXE는 브리지 엔진 자체를 변경해야 할 때만 필요합니다.

NeoForge 전환본은 기존 Fabric 프로필을 덮어쓰지 않고 `코블몬 협동 NeoForge`라는 별도 CurseForge 프로필을 만듭니다. Minecraft 1.21.1 / NeoForge 21.1.256을 사용하며 모드와 FancyMenu 메인 화면은 `manifest-neoforge-v2.json`으로 갱신합니다.

브리지 0.6.2는 자체 모드 9개의 EXE 내장 예비 JAR만 제거한 경량판입니다. 자체 모드는 크기·SHA-256·NeoForge 모드 ID를 검증한 다운로드 캐시 또는 온라인 파일로 설치합니다. 패치기 화면, FancyMenu 이미지·설정, 프로필 아이콘과 작은 예비 목록·로더 JSON은 그대로 유지하며 모드 자체의 기능·자산은 줄이지 않았습니다. 일반 모드 업데이트에는 새 EXE가 필요하지 않습니다. 캐시에 없는 파일을 설치하려면 인터넷 연결이 필요합니다. 활성 온라인 목록은 29모드·13클라이언트파일이며 내장 예비 목록은 종전 24모드 기준입니다.

0.6.2 회귀 150항목 및 격리 통합 400항목을 검증했습니다. 빈 캐시의 전체29모드·13클라이언트파일 설치, 재설치 무변경, 구버전 갱신·백업, 다운로드/SHA 오류 보존, 실제 모드 교체 후 메뉴 다운로드 실패의 롤백·복구를 확인했습니다. 배포 GUI 바이너리도 창 없이 CLI 검사했으며 기존 정적 리소스14개는 원본과 동일한 SHA-256입니다. 실제 게임 실행·시각/청음 검증은 포함하지 않습니다.

앞선 브리지 0.6.1은 TOML 주석이 붙은 Cobblemon·FancyMenu 등의 모드 ID 검사와 해시 파일명으로 다운로드한 Kotlin for Forge 라이브러리 검사를 수정했습니다. 모드와 리소스의 새 온라인 해시가 내장본과 다르면 원격 파일을 받아 업데이트합니다. 당시 빈 캐시의 전체24모드·13클라이언트파일 설치와 회귀63항목을 검증했습니다.

현재 자체 제작 모드 배포 버전:

- 코블몬 모험 메뉴 `0.1.0-alpha.6`
- 코블몬 협동 전투 `0.1.0-alpha.34`
- 코블몬 전설 조우 `0.1.0-alpha.5`
- 코블몬 전설 포켓몬 제단 `0.1.0-alpha.18`
- 쌍둥이 성소 챕터 맵 `0.2.0-alpha.5`
- 협동 메뉴 BGM `1.0.0`
- 두더지 시네마 플레이어 `0.1.0-alpha.7`
- Streamer Shops `0.1.0-alpha.37`

스이쿤 조우 영상은 GitHub Release 자산으로, 스트리머 상점 음성팩 r07은 클라이언트 리소스팩으로 배포합니다. 실제 화면 검수 대기 중인 QHD 타이틀 시안은 배포 목록에 포함하지 않았습니다.

`필드 6` 메뉴 BGM은 클라이언트 전용 `cobblemon-menu-bgm` 모드가 담당합니다. 마스터 채널 기준 30%로 반복 재생하고, 타이틀에서 설정·멀티플레이·접속 화면으로 이동해도 같은 인스턴스를 유지하며 월드 로드 시 정지합니다. 코옵 야생전 모드 JAR과 FancyMenu 레이아웃에는 메뉴 음악 코드나 음원이 포함되지 않습니다.

이 저장소에는 계정 토큰, 서버 비밀번호, 비공개 소스 코드를 올리지 않습니다.
