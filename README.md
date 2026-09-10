# 보건정책관리연구소(준) 홈페이지

고려대학교 보건정책관리연구소(준) 한 페이지 홈페이지. 정적 HTML 한 파일이며 빌드 과정이 없음.

## 파일

| 파일 | 내용 |
|---|---|
| `index.html` | 홈 — 소개, 연구분야·연구센터, Health Politics 편집사무국 |
| `people.html` | 구성원 — 연구위원 11인과 연구분야 |
| `research.html` | 연구과제 — 교외 연구과제 14건 |
| `publications.html` | 논문 — 연구위원 ORCID에서 자동 수집 |
| `service.html` | 대외활동 — 학술지 편집진·학술단체 임원·정부 위원회 |
| `favicon.ico` · `favicon-32.png` · `apple-touch-icon.png` | 브라우저 탭·북마크·모바일 홈화면 아이콘 |
| `CNAME` | 커스텀 도메인 `ihpm.korea.ac.kr` (DNS 등록 완료 후 효력) |
| `.nojekyll` | GitHub Pages의 Jekyll 처리를 끔 |

세 파일은 각각 완결된 HTML이며, 공통 스타일과 국·영문 전환 스크립트가 파일마다 들어 있음. 한 파일의 디자인을 바꾸면 나머지 두 파일도 같이 고쳐야 함.

## 올리는 방법

1. GitHub에서 새 저장소를 만듦 (예: `ihpm-ku`). Public으로 생성.
2. 이 폴더의 파일을 저장소 최상위에 업로드 (`Add file → Upload files`).
3. `Settings → Pages → Build and deployment`에서 Source를 **Deploy from a branch**, Branch를 **main / (root)** 로 지정하고 저장.
4. 1~2분 뒤 `https://<계정>.github.io/<저장소>/` 에서 열림.

## 학교 도메인 연결 (정식 연구소 승인 후)

1. 정보전산처에 `ihpm.korea.ac.kr`의 CNAME 레코드를 `hpolicy.github.io` 로 등록 요청 (신청 완료).
2. DNS 반영 확인 후 `Settings → Pages → Custom domain`에 `ihpm.korea.ac.kr` 입력.
3. 인증서 발급이 끝나면 **Enforce HTTPS** 체크.
4. `CNAME` 파일은 저장소에 이미 포함되어 있음. Pages 설정에서 도메인을 입력하면 GitHub이 같은 내용으로 유지함.

※ DNS가 아직 안 잡힌 상태에서 Custom domain을 입력하면 "domain does not resolve" 경고가 뜸. 등록이 반영될 때까지(보통 수십 분~하루) 기다렸다 다시 시도하면 됨.

## 내용 고치기

고칠 내용이 있는 파일을 고치면 됨. GitHub 웹에서 연필 아이콘으로 편집하고 `Commit changes` 하면 1분 내 반영됨.

- **국문/영문** — 텍스트마다 `data-ko`, `data-en` 두 값이 있음. 둘 다 고쳐야 양쪽에 반영됨.
- **채워야 할 자리** — 연구센터 카드의 `[연계 사이트 링크]`, 건강도시아틀라스 링크 주소.
- **링크 넣기** — 연구센터 카드의 `<span class="chip">건강도시아틀라스 ↗</span>` 를
  `<a class="chip" href="주소" target="_blank" rel="noopener">건강도시아틀라스 ↗</a>` 로 바꾸면 됨.

## Health Politics 최신호

페이지가 열릴 때 Crossref(eISSN 3092-5517)에서 최신호 정보를 받아 자동으로 갱신함. 새 호가 Crossref에 등록되면 손대지 않아도 바뀜.

조회가 실패하면 `index.html`에 적혀 있는 값(현재 Vol. 1, No. 2)이 그대로 보임. 그 값도 가끔 손으로 갱신해 두면 안전함.

## 남은 사항

- 영문 성명은 설립신청서 연구업적서의 표기를 이름-성 순으로 통일함. 오하나 교수는 본인 확인을 거쳐 Hannah Oh로 표기함.
- 논문 목록은 연구위원 11인의 ORCID(pub.orcid.org)에서 페이지 열람 시 자동 수집함. 준연구소 설립(2025년 8월) 이후 학술지 논문만 표시하며, 공저 논문은 1편으로 계산함.
- 누락 논문이 있으면 해당 연구위원이 본인 ORCID에 등록하면 자동 반영됨. 홈페이지 파일은 고칠 필요 없음.
