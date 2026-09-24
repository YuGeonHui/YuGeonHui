## 유건희 · iOS Developer

5년간 iOS 서비스를 개발하며 **레거시 구조 개선, 앱 구동 시간 50% 단축, CI/CD 배포 시간 70% 단축** 등 서비스 성능과 개발 환경 개선을 주도해왔습니다.

운영 중 발생하는 문제를 원인과 지표를 바탕으로 좁히고, 기존 구조를 멈추지 않은 채 점진적으로 개선하는 개발을 중요하게 생각합니다. 기능을 어떻게 구현하는지뿐 아니라 **왜 이 문제를 먼저 해결해야 하는지에 근거를 두고 판단하려 합니다.**

📍 Seoul, South Korea &nbsp;·&nbsp; 📮 ghyu_0906@naver.com &nbsp;·&nbsp; ✍️ [Tech Blog](https://velog.io/@yukh0906/posts) &nbsp;·&nbsp; 💼 [LinkedIn](https://www.linkedin.com/in/yugeonhui/)

---

### 프로젝트

| 프로젝트 | 설명 | 링크 |
|---|---|---|
| **메이플 테마박스** | 넥슨코리아 · 꾸미기 전용 앱에서 생활형 앱으로 확장한 2.0.0 전면 개편 주도 (만 단위 다운로드) — Clean Architecture, 구동 시간 50% 단축 | [App Store](https://apps.apple.com/kr/app/id6471400255) |
| **앗차 (Atcha)** | 출발지·목적지 기반 막차 경로와 출발 시점 안내. 디프만 16기 **iOS 파트장** — Clean Architecture + MVVM, Micro Feature Architecture, AlarmKit | [App Store](https://apps.apple.com/kr/app/id6747877903) · [Repo](https://github.com/Atcha-Project/Atcha-iOS) |
| **삐삐 (Bibbi)** | 하루 한 번 가족에게 사진으로 일상 공유. 디프만 14기 **iOS 파트장(4인)** — Tuist 멀티모듈, ReactorKit. **누적 가입 1,000명 · 디프만 14기 대상** | [App Store](https://apps.apple.com/kr/app/id6475082088) · [Repo](https://github.com/YuGeonHui/14th-team5-iOS) |
| **TTCare** | 에이아이포펫 · 반려동물 종합 헬스케어 앱 (만 단위 다운로드). 홈 전면 리뉴얼, 한국·일본·미국 3개국 출시, IAP 자동갱신구독 | |
| **Tamagotchi** | SwiftUI 다마고치 앱. Swift 6 · Tuist 멀티모듈 · WidgetKit. 모든 설계 결정과 근거를 `ARCHITECTURE.md`에 기록 | [Repo](https://github.com/YuGeonHui/Tamagotchi) |

---

### 이런 걸 해왔습니다

**성능 · 안정성**
- 앱 구동 시간 약 4초 → 약 2초 (**50% 단축**) — SDK 로그인·리소스 다운로드·Firebase 버전 체크의 순차 실행을 TaskGroup 병렬 처리로 전환
- async/await 전면 도입 — Actor로 데이터 레이스 방지, `withCheckedContinuation`으로 콜백 API 래핑, `@MainActor`로 ViewModel UI 업데이트 안전성 확보
- 고해상도 리소스 Memory → Disk → Network 다단계 캐시 설계, 버전·Hash 기반 무효화로 중복 다운로드 방지
- Timer 미해제 + 클로저 강한 참조로 인한 메모리 누수를 Instruments(Leaks, Allocations)로 탐지·해결, Crash-free rate 기준 안정성 관리

**아키텍처 · 레거시 개선**
- 2,000줄 이상 레거시 ViewController를 Presentation · Domain · Data로 분리 (UseCase + Repository)
- StackView + ScrollView 화면을 CompositionalLayout + DiffableDataSource로 마이그레이션
- 서버팀과 협업해 네트워크 / 비즈니스 에러를 분리하는 공통 에러 핸들링 구조 설계
- MVC → MVVM 점진적 전환 및 코드 컨벤션 수립, Texture 기술 부채 검증 후 SwiftUI + Combine 신규 앱 전면 개발

**개발 환경 · CI/CD**
- 사내 내부망 제약으로 Fastlane을 쓸 수 없는 환경에서 Jenkins Pipeline 구축 — 배포 약 10분 → 약 3분 (**70% 단축**)
- Dev · Stage · Live 환경별 파이프라인 분리, 기획자·QA도 버튼 한 번으로 배포 가능

**글로벌 · 결제 · 시스템 기능**
- 한국·일본·미국 3개국 출시 — 국가별 기능을 Target으로 분리하고 공통 코드 공유, String Catalog 다국어 지원
- IAP 자동갱신구독 단독 구현 — Sandbox / 심사 환경 영수증 검증 로직을 분리해 반복 리젝 해결
- Background Modes + Local Notification 반복 알람, Timeline Provider 기반 Widget Animation R&D

**AI 활용**
- 오프라인 이벤트(잠실 롯데월드 등) 웹 서비스 기획·디자인·개발·운영 전 과정 주도 (Next.js) — 메이플 캐릭터 생성 **20만 건 이상** 이용
- Claude · GPT · Gemini 기반 Skill · Agent 하네스를 구성해 개발 절차 표준화

---

### 기술 스택

| | |
|---|---|
| **Language** | Swift |
| **UI** | UIKit · SwiftUI · Texture · WidgetKit |
| **Reactive / Async** | Swift Concurrency (async/await, TaskGroup, Actor) · Combine · RxSwift |
| **Architecture** | Clean Architecture · MVVM · Repository · UseCase · ReactorKit |
| **Library** | Alamofire · SnapKit · Kingfisher |
| **Build · CI** | SPM · CocoaPods · Tuist · Jenkins · Git Flow |
| **Etc** | Firebase (Analytics, Cloud Messaging, Crashlytics) · StoreKit(IAP) · Instruments · JIRA · Figma |

---

### 경력

| 기간 | 회사 | 역할 |
|---|---|---|
| 2024.05 ~ 현재 | **넥슨코리아** | 메이플 R&D실 · iOS 개발자 (G2) |
| 2021.06 ~ 2024.05 | **에이아이포펫** | iOS 개발자 · 대리 |
| 2020.12 ~ 2021.06 | **라임솔루션** | iOS 개발자 · 사원 |

### 학력 · 자격

- 대진대학교 컴퓨터공학과 (2015.03 ~ 2021.02) · 학점 4.11 / 4.5
- 정보처리기사 (2021.09) · SQLD (2022.04)
