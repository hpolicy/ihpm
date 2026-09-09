# 보건정책관리연구소(준) 홈페이지

고려대학교 보건정책관리연구소(준) 한 페이지 홈페이지. 정적 HTML 한 파일이며 빌드 과정이 없음.

## 파일

| 파일 | 내용 |
|---|---|
| `index.html` | 홈 — 소개, 연구분야·연구센터, Health Politics 편집사무국 |
| `people.html` | 구성원 — 연구위원 11인과 연구분야 |
| `research.html` | 연구성과 — 교외 연구과제 14건 |
| `favicon.svg` · `favicon.ico` · `apple-touch-icon.png` | 브라우저 탭·북마크·모바일 홈화면 아이콘 |
| `.nojekyll` | GitHub Pages의 Jekyll 처리를 끔 |

세 파일은 각각 완결된 HTML이며, 공통 스타일과 국·영문 전환 스크립트가 파일마다 들어 있음. 한 파일의 디자인을 바꾸면 나머지 두 파일도 같이 고쳐야 함.

## 올리는 방법

1. GitHub에서 새 저장소를 만듦 (예: `ihpm-ku`). Public으로 생성.
2. 이 폴더의 파일을 저장소 최상위에 업로드 (`Add file → Upload files`).
3. `Settings → Pages → Build and deployment`에서 Source를 **Deploy from a branch**, Branch를 **main / (root)** 로 지정하고 저장.
4. 1~2분 뒤 `https://<계정>.github.io/<저장소>/` 에서 열림.

## 학교 도메인 연결 (정식 연구소 승인 후)

1. 정보전산처에서 서브도메인(예: `ihpm.korea.ac.kr`)을 배정받음.
2. 그 도메인의 DNS에 CNAME 레코드를 `<계정>.github.io` 로 지정해 달라고 요청.
3. 저장소 최상위에 `CNAME` 파일을 만들고 도메인만 한 줄 적음 (예: `ihpm.korea.ac.kr`).
4. `Settings → Pages → Custom domain`에 같은 도메인을 입력하고 **Enforce HTTPS**를 켬.

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

- 영문 성명 표기 — 정혜주 교수(Haejoo Chung) 외 10인은 국문으로 두었음. 확정되면 `data-en` 값에 반영.
- 논문 목록은 아직 없음. 연구위원 11인의 ORCID를 모으면 Crossref에서 자동으로 목록을 만들 수 있음.
