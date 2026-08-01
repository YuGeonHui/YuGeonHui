## iOS Developer

**Swift로 사용자에게 닿는 앱을 만듭니다.** 레거시 구조를 개선하고, 측정 가능한 성능·생산성 개선을 만드는 데 관심이 많습니다.

현재 **넥슨코리아 메이플 R&D실**에서 메이플 테마 박스 iOS 앱을 1인 개발로 담당하고 있습니다.

📍 Seoul, South Korea &nbsp;·&nbsp; 📮 ghyu_0906@naver.com &nbsp;·&nbsp; ✍️ [Tech Blog](https://velog.io/@yukh0906/posts) — Swift Concurrency · GCD 시리즈 정리

---

### 최근 작업

| 프로젝트 | 설명 | 링크 |
|---|---|---|
| **메이플 테마 박스** | 메이플스토리 꾸미기·생활형 앱. Clean Architecture 전면 개편, 구동 시간 50% 단축 · 1인 개발 | [App Store](https://apps.apple.com/kr/app/id6471400255) |
| **앗차 (Atcha)** | 막차 확인 · 택시비 절약 계산 앱. 디프만 16기 **iOS 파트장(2인)** — Clean Architecture + MVVM, Swift Concurrency | [App Store](https://apps.apple.com/kr/app/id6747877903) · [Repo](https://github.com/Atcha-Project/Atcha-iOS) · [My commits](https://github.com/Atcha-Project/Atcha-iOS/commits?author=YuGeonHui) |
| **삐삐 (Bibbi)** | 하루 한 번 가족에게 보내는 생존신고. 디프만 14기 **iOS 파트장(4인)** — Tuist 멀티모듈, ReactorKit | [App Store](https://apps.apple.com/kr/app/id6475082088) · [Repo](https://github.com/depromeet/14th-team5-iOS) |
| **Tamagotchi** | SwiftUI 다마고치 앱. Swift 6 · Tuist 멀티모듈 · WidgetKit. 모든 설계 결정과 근거를 `ARCHITECTURE.md`에 기록 | [Repo](https://github.com/YuGeonHui/Tamagotchi) |

---

### 이런 걸 해왔습니다

**성능 · 생산성**
- 앱 구동 시간 4초 → 2초 (**50% 단축**) — 순차 초기화를 TaskGroup 병렬 처리로 전환, async/await 전면 도입
- 배포 시간 10분 → 3분 (**70% 단축**) — 사내 내부망 제약으로 Fastlane을 못 쓰는 환경에서 Jenkins Pipeline 단독 구축. 기획자·QA도 버튼 하나로 배포 가능해져 배포 병목 해소

**아키텍처**
- 2,000줄 규모 God ViewController를 Presentation–Domain–Data로 분리 (UseCase + Repository)
- StackView + ScrollView 레거시 UI를 UICompositionalLayout + DiffableDataSource로 마이그레이션
- MVC → MVVM 점진적 마이그레이션과 코드 컨벤션 자체 수립
- Texture의 기술 부채를 인지하고 검증 → SwiftUI + Combine 신규 앱 전면 개발로 연결

**글로벌 · 결제**
- 한국·일본·미국 3개국 출시, Target 분리 기반 다국어 구조 설계
- IAP 자동갱신구독 전체 라이프사이클 단독 구현 — 갱신·해지·환불 상태 관리, 환경별 영수증 검증 분리로 심사 리젝 해결

**AI 활용**
- Claude / GPT / Gemini 하네스(Skill · Agent)를 직접 구성해 코드 리뷰·레거시 리팩토링에 적용, 아키텍처 규칙 준수를 일관되게 점검
- 오프라인 이벤트 웹 서비스를 기획부터 개발까지 주도 (Next.js) — 캐릭터 생성 10만 건 이상 이용

---

### 기술 스택

| | |
|---|---|
| **Language** | Swift · Kotlin |
| **UI** | SwiftUI · UIKit · Texture · WidgetKit |
| **Async** | Swift Concurrency · RxSwift · Combine |
| **Architecture** | Clean Architecture · MVVM · ReactorKit |
| **Build · CI** | Tuist · SPM · Jenkins · GitHub Actions |
| **Etc** | AVFoundation · StoreKit(IAP) · Firebase · Instruments |

---

### 경력

| 기간 | 회사 | 역할 |
|---|---|---|
| 2024.05 ~ 현재 | **넥슨코리아** | 메이플 R&D실 · iOS (G2) |
| 2021.06 ~ 2024.05 | **에이아이포펫** | iOS · 대리 |
| 2020.12 ~ 2021.06 | **라임솔루션** | iOS · 사원 |
