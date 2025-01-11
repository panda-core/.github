# PANDA

**P**NP **A**ll **N**ew **D**esign **A**rchitecture  
사내 디자인 시스템 & UI 프레임워크 구축·운영을 위한 **GitHub Organization**

<br />

## Repository Structure

| Repository              | Purpose                                    | Description                                                         |
|-------------------------|--------------------------------------------|---------------------------------------------------------------------|
| **panda-design-docs**   | 요구사항 정의, 설계 원칙, 비전 선언문 등 **문서 중심** 레포      | - 마크다운 기반 문서<br/>- GitHub Pages / Confluence / Notion 등 협업 툴 연동     |
| **panda-design-tokens** | 색상·간격·타이포그래피 등 다양한 **디자인 토큰** 관리           | - JSON/TS/SCSS 등 포맷 구성<br/>- Figma 연동 & 자동 변환 스크립트 (NPM 배포)         |
| **panda-ui-framework**  | **Core/Clay/Mold** 계층 구조의 UI 컴포넌트 라이브러리    | - Vue.js 3 지원<br/>- Storybook 기반 컴포넌트 문서화<br/>- NPM 패키지로 배포 및 버전 관리 |
| **panda-prototypes**    | POC(Proof Of Concept)·실험 기능 등 **프로토타입** 레포 | - 제품별 샘플 구현<br/>- 안정화 시 `panda-ui-framework`로 통합                    |
| **panda-docs-site**     | (선택) 검색·정적 사이트 형태로 **문서화** 운영              | - 문서 검색, 버전 관리<br/>- UI/UX 가이드 웹사이트로 구성                             |

<br />

## Workflow

1. **Branch Strategy**
    - `main`: Production-ready branch (실제 배포 버전)
    - `develop`: 공동 개발 및 테스트용 브랜치
    - `feature/*`: 기능별 브랜치 → 작업 완료 후 `develop`에 머지

2. **CI/CD**
    - GitHub Actions로 **테스트**, **빌드**, **배포**를 자동화
    - `panda-design-tokens`: 디자인 토큰 변경 시 → 변환 스크립트 후 NPM 배포
    - `panda-ui-framework`: 태그(`v1.0.0`) 지정 시 → 자동 NPM 릴리즈 & Storybook 업데이트

3. **Release Management**
    - [Semver (유의적 버전)](https://semver.org/lang/ko/) (Major.Minor.Patch)
    - GitHub Releases를 통한 릴리즈 노트 및 태깅(`v1.0.0`)

<br />

## Contact & Contribution

- **Issues / Pull Requests**: [Issue 트래커](./issues) 또는 [Pull Request](./pulls)를 통해 제안 및 버그 리포트
- **Collaboration**: 기여 가이드(Commit/PR 규칙 등)는 각 레포지토리의 `CONTRIBUTING.md` 참고

<br />

<sup>© 2025 panda – All rights reserved.</sup>  
