# 오버 스터디! — GitHub Pages 올리기

## 1. Firebase 규칙 설정 (한 번만)
Firebase 콘솔 → Realtime Database → **규칙** 탭에 아래를 붙여넣고 **게시**:

```
{
  "rules": {
    ".read": true,
    ".write": true,
    "students": { ".indexOn": ["cls"] }
  }
}
```
※ 주소를 아는 사람은 누구나 읽고 쓸 수 있는 규칙입니다. 학급용으로만 쓰고, 개인정보는 넣지 마세요.

## 2. GitHub에 올리기
1. GitHub에서 새 저장소를 만듭니다 (Public). 예: `overstudy`
2. 저장소 화면에서 **Add file → Upload files** 로 `index.html` 을 올리고 Commit.
3. **Settings → Pages → Build and deployment**: Source = *Deploy from a branch*, Branch = `main` / `(root)` → Save.
4. 1~2분 뒤 `https://<GitHub이름>.github.io/<저장소이름>/` 로 접속할 수 있습니다.

## 참고
- 같이 요리하기·경쟁 모드는 Firebase의 `rooms` 경로를 사용합니다 (위 규칙에 이미 포함).
- AI 문제 만들기 기능은 이 사이트에서는 쓸 수 없습니다. 직접 입력하는 문제 설정은 그대로 됩니다.
