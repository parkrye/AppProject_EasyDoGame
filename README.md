# EasyDoGame

광고 · 네트워크 없는 안드로이드 간단 게임 모음. 체스 · 7선 바둑 · 오목(AI 3단계) · 벽돌깨기(클래식 · 숫자 블록) · 수박게임 · 2048 · 3매치 · 미니 골프(기본 · 랜덤 코스) · 당구(4구 · 3쿠션 · 8볼) · 테트리스 10종. 모든 게임 이어하기 · 게임별 기록. 가볍고 빠르게(APK 약 1.4MB), 데이터는 기기 밖으로 나가지 않음. EasyDo 시리즈.

버그 · 제안은 [Issues](../../issues)에.

## 다운로드

최신 버전 0.2.0 — [Releases](https://github.com/parkrye/AppProject_EasyDoGame/releases)에서 `EasyDoGame-<버전>.apk`를 받아 설치. Android 8.0 이상.

- 처음 설치 시 "출처를 알 수 없는 앱" 설치 허용 필요. Play 프로텍트가 검사 화면을 띄울 수 있음
- 업데이트는 새 APK를 같은 방식으로 덮어 설치. 기록 · 설정 유지
- 앱 안 `설정 → 앱 정보 → 새 버전 받기`로 Releases 페이지를 열 수 있음 (자동 업데이트 알림 없음)
- 서명 인증서 SHA-256: `d0527f3e46788d62f1b40accbc1a95bede62c010ca4cf9805f44a51698e3a3b3`
  (`apksigner verify --print-certs EasyDoGame-<버전>.apk`로 확인). 각 Release 본문에 APK SHA-256도 기재

## 기능

| 게임 | 내용 |
|---|---|
| 체스 | 캐슬링 · 앙파상 · 승진 · 체크메이트 · 스테일메이트 · 50수 · 3회 반복 · 기물 부족. AI 쉬움 · 보통 · 어려움. 백/흑 선택, 무르기 |
| 7선 바둑 | 7×7, 따냄 · 자충수 금지 · 패(위치 초과패), 패스 2회 종국 · 기권. 중국식 계가, 덤 8.5. 종국 시 사석 추정 후 탭으로 수정. AI 쉬움 · 보통 · 어려움 |
| 오목 | 15×15 자유룰(5목 이상 승, 금수 없음). AI 쉬움 · 보통 · 어려움. 두 번 탭 착수, 무르기 |
| 벽돌깨기 | 클래식: 5개 스테이지 패턴 반복, 내구도 1~3 벽돌, 목숨 3, 스테이지마다 속도 증가. 숫자 블록: 7열 판, 끌어서 조준 · 공 전부 연속 발사, 맞을 때마다 숫자 -1(0이면 파괴), 처음 바닥에 닿은 공 자리가 다음 발사 위치, 공 +1 아이템, 줄 기믹(가로 · 세로 · 십자), 턴마다 한 줄 하강 · 새 줄 생성, 바닥 줄 도달 시 종료. 회수 · 빨리 감기. 모드별 최고 점수 |
| 수박게임 | 11단계 과일, 원형 물리(중력 · 충돌 · 마찰), 같은 과일 합치기, 경계선 초과 시 종료 |
| 2048 | 4×4 표준 규칙, 스와이프, 무르기 1회, 2048 이후 계속 |
| 3매치 | 8×8 · 보석 6종(색 + 모양), 연쇄 배수, 가능한 수 없으면 섞기, 30수로 시작 · 보석 15개 깰 때마다 +1(상한 없음), 힌트 |
| 미니 골프 | 기본 9홀(벽 · 모래 · 물 · 경사), 당겨서 치기, 홀당 최대 10타, 9홀 총타수. 랜덤 코스: 매번 새로 만드는 9홀(여러 외곽 · 벽 · 블록 · 모래 · 다리 있는 물길 · 경사), 홀인 가능한 경로가 있는 홀만 사용, 경로 길이로 파 산정. 코스별 최고 기록 |
| 당구 | 4구(빨간 공 둘 +1, 상대 수구 -1, 10점) · 3쿠션(두 적구 전 쿠션 3회, 5점) · 8볼(그룹 배정 · 파울 · 볼 인 핸드 · 8번 규칙, 콜샷 없음). 당점(끌어치기 · 밀어치기 · 좌우 회전), 드래그 조준 · 미세 조정 · 세기, 가이드선. AI 쉬움 · 보통 · 어려움 또는 2인 |
| 테트리스 | 표준 7종, SRS 회전 · 월킥, 7-bag, 홀드, 다음 5개, 고스트, 소프트/하드 드롭, 레벨별 낙하 속도, 라인 점수 100/300/500/800×레벨. 버튼(길게 누르면 반복) + 스와이프 |

이어하기: 나가거나 앱이 꺼져도 하던 게임을 이어서 진행(새 게임은 버튼). 실시간 게임은 일시정지 상태로 복원(탭하여 계속). 이어할 판이 없으면 들어갈 때 설정 창(난이도 · 모드) 또는 시작 창부터 표시.

기록(하단 기록 탭 · 게임 화면 상단 아이콘): 플레이 횟수 · 총 플레이 시간 · 최근 20판, 대전 게임은 난이도별(당구는 2인 포함) 승 · 무 · 패, 점수 게임은 최고 점수(골프는 최소 타수, 숫자 블록 · 랜덤 코스는 따로).

설정:

- `화면`: 배경화면 색 사용(Android 12 이상, 기본 꺼짐)
- `데이터`: 백업 만들기 · 백업에서 복원(파일 하나 `easydogame-backup-yyyy-MM-dd.json`, 복원 전 확인 대화상자)
- `앱 정보`: 앱 정보(버전) · 새 버전 받기(Releases 페이지) · 오픈소스 라이선스

## 개인정보

인터넷 권한 없음 · 광고 없음 · 수집 · 전송 없음.

- 계정 · 광고 · 사용 통계 · 오류 보고 없음
- 기록 · 진행 중 게임 · 설정은 기기 안에만 저장. 앱 삭제 시 함께 삭제 (Android 클라우드 백업 제외)
- 앱 안 백업 파일은 사용자가 고른 위치에만 저장. 기기를 바꿀 때는 백업 파일을 옮겨 복원

## EasyDo 시리즈

| 앱 | 용도 | 플랫폼 |
|---|---|---|
| [EasyDoDraw](https://github.com/parkrye/MultiProject_EasyDoDraw) | 그림 · 애니메이션 | Android · Windows |
| [EasyDoWrite](https://github.com/parkrye/AppProject_EasyDoWrite) | 소설 · 글쓰기 | Android |
| [EasyDoRead](https://github.com/parkrye/AppProject_EasyDoRead) | 책 · 문서 읽기 | Android |
| [EasyDoShelve](https://github.com/parkrye/AppProject_EasyDoShelve) | 웹 소설 서재 | Android |
| [EasyDoPhoto](https://github.com/parkrye/AppProject_EasyDoPhoto) | 카메라 · 사진 편집 | Android |
| [EasyDoDiet](https://github.com/parkrye/AppProject_EasyDoDiet) | 식단 · 운동 기록 | Android |
| [EasyDoZip](https://github.com/parkrye/AppProject_EasyDoZip) | 파일 · 압축 관리 | Android |
| [EasyDoGame](https://github.com/parkrye/AppProject_EasyDoGame) | 미니 게임 모음 | Android |
| [EasyDoMix](https://github.com/parkrye/AppProject_EasyDoMix) | 영상 · 오디오 편집 | Android |
| [EasyDoRecord](https://github.com/parkrye/AppProject_EasyDoRecord) | 녹음 | Android |
| [EasyDoStudio](https://github.com/parkrye/DesktopProject_EasyDoStudio) | 화면 녹화 · 영상 편집 | Windows |

## 라이선스

MIT License · © parkrye. 포함된 서드파티 라이브러리 고지는 앱 안 `설정 → 앱 정보 → 오픈소스 라이선스`에서 확인.
