# tapllul.com

tapllul 공식 홈페이지. 빌드 도구 없는 정적 사이트이며 GitHub Pages로 배포됩니다.

## 구성

| 파일 | 설명 |
| --- | --- |
| `index.html` | 홈페이지 전체 (HTML + CSS + JS 한 파일) |
| `404.html` | 없는 경로 접근 시 표시 |
| `CNAME` | GitHub Pages 커스텀 도메인 (`tapllul.com`) |
| `favicon.svg` | 파비콘 |
| `robots.txt`, `sitemap.xml` | 검색엔진용 |
| `.nojekyll` | Jekyll 처리 비활성화 |

## 로컬에서 보기

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## 수정하기

`index.html` 한 파일만 고치면 됩니다. 한국어/영어는 같은 위치에 나란히 들어 있습니다.

```html
<span class="ko">한국어 문장</span><span class="en">English sentence</span>
```

우측 상단 `EN` / `한국어` 버튼이 `<html data-lang>` 값을 바꾸고, CSS가 해당 언어만 표시합니다.
선택한 언어와 다크모드 설정은 `localStorage`에 저장됩니다.

색상은 `index.html` 상단 `:root` 의 CSS 변수에서 한 번에 바꿀 수 있습니다.

## 배포

`main` 브랜치에 푸시하면 GitHub Pages가 자동으로 반영합니다 (보통 1분 이내).

## DNS (후이즈)

| 타입 | 호스트 | 값 |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | cwh1981.github.io |
