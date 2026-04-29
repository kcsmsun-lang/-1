diff --git a/README.md b/README.md
new file mode 100644
index 0000000000000000000000000000000000000000..6aee228541cd5e0e15efb3be034d8e9ea62c6b43
--- /dev/null
+++ b/README.md
@@ -0,0 +1,13 @@
+# 전주시청 시내버스 홍보 정적 사이트
+
+이 저장소는 `index.html` 기반의 정적 웹사이트입니다.
+
+## GitHub Pages 배포 방법
+
+1. GitHub 저장소의 **Settings → Pages**로 이동합니다.
+2. **Build and deployment** 항목에서 **Source: GitHub Actions**를 선택합니다.
+3. `main` 브랜치에 푸시하면 `.github/workflows/deploy-pages.yml` 워크플로가 실행되어 자동 배포됩니다.
+
+## 로컬 미리보기
+
+별도 빌드 없이 브라우저에서 `index.html` 파일을 직접 열어 확인할 수 있습니다.
