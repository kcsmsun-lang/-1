 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 8b137891791fe96927ad78e64b0aad7bded08bdc..7a2332f822f275dbdec140457542c427ebfc3a8f 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,83 @@
+# 홍보자료 일별 아카이브 (GitHub Pages용)
 
+이 프로젝트는 **HTML/CSS/JavaScript만 사용한 정적 웹사이트**입니다.
+홍보 이미지를 날짜별로 묶어서 카드 형태로 보여줍니다.
+
+- 메인 파일: `index.html`
+- 이미지 폴더: `assets/`
+
+---
+
+## 1) GitHub Pages로 바로 열기
+
+1. 이 저장소를 GitHub에 업로드합니다.
+2. GitHub 저장소 → **Settings** → **Pages**로 이동합니다.
+3. **Source**를 `Deploy from a branch`로 선택합니다.
+4. Branch를 `main`(또는 사용하는 브랜치) / 폴더는 `/ (root)`로 선택 후 저장합니다.
+5. 잠시 후 발급되는 사이트 주소로 접속하면 됩니다.
+
+---
+
+## 2) 새 홍보자료 추가하는 가장 쉬운 방법
+
+### Step A. 이미지 파일 넣기
+
+1. `assets/` 폴더에 이미지 파일을 넣습니다.
+   예: `assets/2026-05-06-event-banner.png`
+
+### Step B. `index.html`의 `promotions` 배열에 항목 1개 추가
+
+`index.html` 안에 아래와 같은 코드가 있습니다.
+
+```js
+const promotions = [
+  {
+    title: "2026-05-05 전북현대모터스 홈경기 특별노선1994 운행안내",
+    date: "2026-05-05",
+    description:
+      "홈경기 당일 특별노선 1994 운행 시간과 탑승 위치를 안내하는 홍보자료입니다.",
+    image: "assets/2026-05-05-jeonbuk-special-route-1994.svg",
+    download: "assets/2026-05-05-jeonbuk-special-route-1994.svg",
+  },
+];
+```
+
+여기에 같은 형식으로 객체를 추가하면 됩니다.
+
+```js
+{
+  title: "2026-05-06 어린이날 특별 이벤트",
+  date: "2026-05-06",
+  description: "어린이날 현장 이벤트와 경품 안내",
+  image: "assets/2026-05-06-event-banner.png",
+  download: "assets/2026-05-06-event-banner.png",
+}
+```
+
+> **중요:** `date`는 꼭 `YYYY-MM-DD` 형식(예: `2026-05-06`)으로 입력하세요.
+
+---
+
+## 3) 화면 동작 방식
+
+- 같은 `date` 값을 가진 항목끼리 자동으로 묶입니다.
+- 각 항목은 카드로 표시됩니다.
+- 카드에는 자동으로 아래 정보가 나옵니다.
+  - 제목
+  - 날짜
+  - 설명
+  - 다운로드 버튼
+
+---
+
+## 4) 로컬에서 미리 보기
+
+파일을 그냥 더블클릭해서 `index.html`을 열어도 동작합니다.
+
+또는 간단한 로컬 서버를 쓰고 싶다면:
+
+```bash
+python -m http.server 8000
+```
+
+브라우저에서 `http://localhost:8000` 접속.
 
EOF
)
