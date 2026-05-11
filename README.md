<h1 align="center">Na Keaunsol</h1>
<p align="center">
  Backend Engineer · 4년차 · Spring · Elasticsearch · HR 도메인 → AI 확장 중
</p>

<p align="center">
  <a href="https://keaunsolna.github.io/keaunsolNa/">📄 Portfolio</a> ·
  <a href="https://ks-awesome.notion.site/Na_KeaunSol_Coding_Study-b341f3bb4bc943c5b698e9808306f44c">📚 Study Archive</a> ·
  <a href="mailto:knsol1992@naver.com">✉️ Email</a>
</p>

---

### 어떤 개발자인가

- **HR 도메인 SI 4년차** — SK바이오로직스 · SL글로벌 · 포스코인터내셔널 HR 플랫폼에서 사회보험·퇴직금·연말정산 모듈 설계·구현
- **Spring + Elasticsearch + Oracle** — Oracle 파편화 코드 체계를 4단계 계층 ES 인덱스로 재설계, Nori 분석기 기반 한국어 검색
- **AI 도구를 직접 만들어 쓰는 백엔드** — Claude Code · Groq · DeepL API 기반 일일 트렌드 수집기, LeetCode 자동 리뷰 봇 운영
- **운영까지 책임지는 사람** — Heroku R14 메모리 트러블슈팅 · G1GC 튜닝 · GitHub Actions → AWS ECR → EC2(SSM) 자동 배포

---

### 🛠 핵심 프로젝트

#### [KNOCK](https://github.com/keaunsolNa/Knock) — 영화·공연 개봉일 리마인더 (백엔드 단독)
5개 플랫폼(KOFIC · CGV · MEGABOX · LOTTE · KOPIS) 동시 크롤링 → Elasticsearch 인덱싱 → FCM 푸시 알림.

- **Template Method 패턴**으로 플랫폼별 파서 추상화 — 신규 플랫폼 추가 시 기존 코드 무수정
- **OAuth2 Strategy 패턴** (Kakao/Naver/Google) + **JWT 이중 토큰** (Access in-memory / Refresh HttpOnly·Secure)
- **유사도 기반 중복 병합 로직** 직접 설계 — 플랫폼 간 동일 작품 단일 레코드 통합
- **Heroku R14 메모리 트러블슈팅** — 스케줄링 최적화 + G1GC 튜닝(`-Xms512m -Xmx2g`)으로 해결

🔗 [백엔드 서버](https://github.com/keaunsolNa/knock-back-server) · [크롤링 서버](https://github.com/keaunsolNa/knock_crawling) · [라이브 데모](https://knock-six.vercel.app)

#### [dev-trends](https://github.com/keaunsolNa/dev-trends) — 일일 개발 트렌드 자동 수집기
Hacker News · Stack Overflow · GitHub Discussions에서 매일 08:00 KST 자동 수집 → 한국어 번역 → Slack 전파 + MD 리포트 Git 자동 커밋.

- 자체 스코어링 공식: `log10(upvotes+1)·1.0 + log10(comments+1)·1.5 + log10(views+1)·0.3`
- **DeepL → deep-translator 2단계 폴백**으로 번역 안정성 확보
- GitHub Actions cron 기반 무인 운영

#### [leetCodeHelper](https://github.com/keaunsolNa/leetCodeHelper) — LeetCode 풀이 자동화 (Spring Boot 4 · Java 24)
LeetCode GraphQL 연동, IntelliJ External Tool 통합 제출, Accepted 시 Groq(`llama-3.3-70b-versatile`) 기반 한국어 코드 리뷰 자동 생성 + Git UnSolved → Solved 자동 이동·커밋·푸시.

#### POST EAT — 음식 사진 기반 푸드 다이어리 (백엔드/DB 전담, 진행 중)
TroisLab 3인 팀, 린 스타트업 + 애자일 스프린트 기반.

- **Flyway DB 마이그레이션** — 스키마 변경 이력 코드 관리, 팀 간 동기화 자동화
- **JPA AOP 쿼리 타이밍 로깅** — 모든 리포지토리 호출 실행시간 자동 수집, 병목 조기 발견
- **Docker 멀티스테이지(Alpine) 빌드** + GitHub Actions → AWS ECR → EC2(SSM) 자동 배포

#### Properties Server — HR 공통 코드 서버 (회사 프로젝트 · 비공개)
Oracle에 파편화된 수백 개 공통코드를 **BizUnit → CodeSys → CodeKind → Code 4단계 계층**으로 재설계, 4개 독립 ES 인덱스로 분리.

- Spring Data ES Bulk API 기반 Oracle JPA → ES 대량 이관 파이프라인
- ID/코드류는 `Keyword`, 명칭/설명류는 `Text + Nori` 하이브리드 매핑
- Spring Boot 3.x + Java/Kotlin 혼합 구성

---

### 🧰 기술 스택

**주력 (실무 1년+)** &nbsp; Java · Spring Boot · Spring Security · JSP · Oracle · PL/SQL · Vue.js

**실무 경험** &nbsp; Kotlin · JPA · Elasticsearch · Nori · MariaDB · Redis · Docker · GitHub Actions · AWS(EC2/S3/CloudFront) · Heroku · React · Next.js

**학습/확장** &nbsp; Python · FastAPI · Multi-Agent · RAG · gRPC · Kafka

---

### 📚 학습 & 기록

- [**PersonalStudy**](https://github.com/keaunsolNa/PersonalStudy) — Notion ↔ GitHub 동기화 학습 노트 (270+ 문서, 8개 카테고리)
- [**Coding_Test**](https://github.com/keaunsolNa/Coding_Test) · [**AlgorithmStudy**](https://github.com/keaunsolNa/AlgorithmStudy) — 백준·프로그래머스
- [![solved.ac](https://mazassumnida.wtf/api/v2/generate_badge?boj=knsol1992)](https://solved.ac/knsol1992/) Platinum IV · 3,500+ 문제 · 560일 최장 스트릭

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=keaunsolNa&show_icons=true&theme=tokyonight" />
</p>
