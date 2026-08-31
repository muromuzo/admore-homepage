# 애드모어 ADMORE 홈페이지

퍼포먼스 마케팅 · 광고 대행사 **애드모어(ADMORE)** 공식 홈페이지 정적 사이트.

## 구성

```
index.html            # 원페이지 랜딩 (스타일·스크립트 인라인)
robots.txt            # 크롤러 허용 + 사이트맵 위치
sitemap.xml           # 검색엔진 제출용
site.webmanifest      # PWA/앱 아이콘 메타
favicon.ico           # 16/32/48 멀티사이즈
naver*.html           # 네이버 서치어드바이저 소유확인 파일 (건드리지 말 것)
assets/
  admore-h.png        # 가로형 로고
  admore-stack.png    # 스택형 로고
  admore-mark.png     # 심볼만 (파비콘 원본)
  og-image.png        # 1200x630 공유 카드
  favicon-32.png
  apple-touch-icon.png
  icon-192.png / icon-512.png
```

## 로컬 확인

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## 배포

`main` 브랜치 푸시 → **Vercel** 프로젝트 `admore-homepage` 자동 배포.

- 운영 도메인: <https://www.애드모어.com> (`www.xn--hy1bz3ifpkxja.com`)
- apex(`애드모어.com`)는 www로 308 리다이렉트 → **canonical은 www**

> ⚠️ 커밋 author를 `muromuzo`로 할 것. 다른 계정 이메일로 커밋하면
> Vercel이 "Git author not authorized"로 배포를 차단한다.

## SEO 체크리스트

- [x] title / description / canonical / robots 메타
- [x] Open Graph + Twitter Card (og-image 1200x630)
- [x] 파비콘·앱 아이콘·webmanifest
- [x] 구조화 데이터 (Organization / WebSite / Service)
- [x] robots.txt · sitemap.xml
- [x] 웹폰트 preconnect (렌더 차단 완화)
- [ ] Google Search Console 등록 + 사이트맵 제출
- [ ] 네이버 서치어드바이저 사이트맵 제출 (소유확인 파일은 이미 배치됨)

## 브랜드

- Navy `#06235B`
- Blue `#1D6BE5`
