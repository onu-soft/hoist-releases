# Hoist — Releases

**Hoist** 데스크톱 앱의 배포·자동 업데이트 채널입니다.

- 📦 **다운로드**: [Releases](https://github.com/onu-soft/hoist-releases/releases) 페이지에서 최신 설치 파일을 받으세요.
  - macOS (Apple Silicon): `Hoist.dmg`
  - Windows: `Hoist.exe`
- 🔄 **자동 업데이트**: 앱이 아래 매니페스트를 주기적으로 확인해 새 버전을 알립니다.
  - `https://raw.githubusercontent.com/onu-soft/hoist-releases/main/latest.json`

> 이 저장소는 빌드 산출물(설치 파일)과 업데이트 매니페스트만 호스팅합니다.
> 앱 소스 코드는 비공개 저장소에서 관리됩니다.

## 자동 업데이트 동작

1. 앱 실행 시 `latest.json`(minisign 서명 검증)을 fetch
2. 설치된 버전보다 높은 버전이 있으면 업데이트 모달 표시
3. 사용자가 설치를 승인하면 다운로드 → 서명 검증 → 설치 → 재시작

## 설치 (macOS)

코드사인/공증 전 빌드는 Gatekeeper 경고가 뜰 수 있습니다.
`Hoist.dmg` 를 열어 Applications 로 드래그한 뒤, 첫 실행 시 앱을 **우클릭 → 열기**로 실행하세요.
