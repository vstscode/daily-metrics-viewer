# Onto SDK GitHub Pages 배포

## 배포 파일

GitHub Pages에 이 폴더의 파일을 올립니다.

```text
index.html
README.md
```

`index.html`은 Supabase DB를 직접 바라봅니다.

## 접속 게이트

`index.html`에는 가벼운 ID/PW 게이트가 들어 있습니다. 실제 접속 정보는 공개 repository에 적지 않습니다.

이 인증은 GitHub Pages 정적 페이지 안에서 처리하는 가벼운 접속 게이트입니다. 서버 인증이 아니므로 강한 보안으로 보면 안 됩니다.

## GitHub Pages 설정

1. GitHub에서 새 public repository를 만듭니다.
2. 이 폴더의 `index.html`을 repository root에 업로드합니다.
3. repository `Settings > Pages`로 이동합니다.
4. `Build and deployment`에서 아래처럼 설정합니다.

```text
Source: Deploy from a branch
Branch: main
Folder: /root
```

5. 저장 후 표시되는 Pages URL로 접속합니다.

예상 URL 형식:

```text
https://{github-id}.github.io/{repository-name}/
```

## 진짜 ID/PW 보안이 필요할 때

GitHub Pages는 서버단 Basic Auth를 지원하지 않습니다. 실제 인증이 필요하면 아래 중 하나를 써야 합니다.

```text
Cloudflare Access 앞단 적용
Cloudflare Pages Functions
Netlify/Vercel middleware
사내망 프록시 인증
```

현재 데이터가 공개되어도 문제없는 통계 데이터라면 이 HTML 게이트만으로도 일반적인 우발 접근 차단 용도로는 충분합니다.
