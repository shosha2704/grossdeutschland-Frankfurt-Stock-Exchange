# 🔥 초간단 Firebase 설정 (10분 완성)

## ⏱️ 시간별 단계

### 1단계: Firebase 프로젝트 만들기 (2분)

1. **https://console.firebase.google.com/** 접속
2. **"프로젝트 추가"** 클릭
3. 이름 입력: `stock-game` (원하는 이름)
4. **Google 애널리틱스 → 끄기** 선택
5. **"프로젝트 만들기"** 클릭하고 완료될 때까지 대기

---

### 2단계: Realtime Database 활성화 (2분)

1. 왼쪽 메뉴에서 **"빌드"** → **"Realtime Database"** 클릭
2. **"데이터베이스 만들기"** 클릭
3. 위치: 아무거나 선택 (예: us-central1)
4. **"테스트 모드에서 시작"** 선택 ⭐ **중요!**
5. **"사용 설정"** 클릭

---

### 3단계: Firebase 구성 정보 복사 (3분)

1. 왼쪽 상단 **⚙️ (프로젝트 설정)** 클릭
2. 아래로 스크롤하여 **"내 앱"** 섹션 찾기
3. **"</>" (웹 앱)** 아이콘 클릭
4. 앱 닉네임: `web` (아무거나)
5. **Firebase 호스팅 체크박스는 체크 안 함**
6. **"앱 등록"** 클릭
7. 화면에 나타나는 코드 중 **이 부분만** 복사:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "stock-game-xxxxx.firebaseapp.com",
  databaseURL: "https://stock-game-xxxxx-default-rtdb.firebaseio.com",
  projectId: "stock-game-xxxxx",
  storageBucket: "stock-game-xxxxx.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdefgh"
};
```

---

### 4단계: HTML 파일에 붙여넣기 (3분)

1. **Firebase_설정_가이드.md** 폴더에 있는 **index.html** 파일을 메모장으로 열기
   (우클릭 → 연결 프로그램 → 메모장)

2. **Ctrl+F**로 `YOUR_API_KEY` 검색

3. 찾아진 부분:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    ...
```

4. 이 부분을 **3단계에서 복사한 코드**로 **통째로 교체**

5. **저장** (Ctrl+S)

---

## ✅ 완료! 이제 사용 가능

### GitHub Pages에 업로드하면:
```
https://당신아이디.github.io/repository/
```

### 모든 사용자가:
- ✅ 회원가입 가능
- ✅ 로그인 가능  
- ✅ 거래 가능
- ✅ 계좌이체 가능
- ✅ 실시간 데이터 공유

---

## 🎬 실제 예시

### Firebase에서 복사한 코드:
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyA1B2C3D4E5F6G7H8I9J0",
  authDomain: "my-stock-12345.firebaseapp.com",
  databaseURL: "https://my-stock-12345-default-rtdb.firebaseio.com",
  projectId: "my-stock-12345",
  storageBucket: "my-stock-12345.appspot.com",
  messagingSenderId: "987654321",
  appId: "1:987654321:web:abc123def456"
};
```

### HTML에서 찾은 부분:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",  // ← 이 전체를
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    databaseURL: "https://YOUR_PROJECT_ID-default-rtdb.firebaseio.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

### 교체 후:
```javascript
const firebaseConfig = {
    apiKey: "AIzaSyA1B2C3D4E5F6G7H8I9J0",  // ← 복사한 것으로
    authDomain: "my-stock-12345.firebaseapp.com",
    databaseURL: "https://my-stock-12345-default-rtdb.firebaseio.com",
    projectId: "my-stock-12345",
    storageBucket: "my-stock-12345.appspot.com",
    messagingSenderId: "987654321",
    appId: "1:987654321:web:abc123def456"
};
```

---

## ⚠️ 주의사항

### ❌ 잘못된 방법:
- apiKey만 바꾸기
- 따옴표 지우기
- 쉼표 빼먹기

### ✅ 올바른 방법:
- **전체 { } 블록을 통째로 교체**
- 따옴표와 쉼표 그대로 유지
- 복사-붙여넣기만 하기

---

## 🆘 문제 해결

### "Firebase 연결 실패" 오류
→ firebaseConfig 코드를 제대로 붙여넣었는지 확인

### "권한 거부" 오류  
→ Firebase Console에서 "테스트 모드"로 설정했는지 확인

### 데이터가 안 보여요
→ Firebase Console > Realtime Database > 데이터 탭에서 확인

---

## 🎉 성공하면?

1. 회원가입 → 로그인
2. 주식 매수
3. 친구에게 링크 공유
4. 친구도 회원가입 → 로그인
5. 서로 계좌이체 가능!

**모두 같은 데이터베이스를 공유합니다!**
