# 🐢 터틀런 (Turtle Run) - NFC 러닝 게임

> NFC 키링을 태그하고 걸으면서 거북이를 키워보세요!

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Web-orange)

---

## 📖 목차

1. [프로젝트 소개](#-프로젝트-소개)
2. [주요 기능](#-주요-기능)
3. [빠른 시작](#-빠른-시작)
4. [상세 가이드](#-상세-가이드)
5. [기술 스택](#-기술-스택)
6. [커스터마이징](#-커스터마이징)
7. [FAQ](#-faq)
8. [라이선스](#-라이선스)

---

## 🎮 프로젝트 소개

**터틀런**은 NFC 키링과 스마트폰을 이용한 러닝 게임입니다. 실제로 걸으면서 가상의 거북이를 키우고, 특별한 장소(거북섬)에 도착하면 아이템을 받을 수 있어요!

### 핵심 컨셉

```
NFC 키링 태그 → 거북이 알 획득 → 러닝 시작 → 거북이 성장 → 거북섬 도착 → 아이템 획득
```

### 특징

- 🔑 **NFC 키링 연동**: 키링만 태그하면 자동으로 게임 시작
- 🗺️ **실시간 GPS 추적**: OpenStreetMap 기반 경로 기록
- 🐢 **단계별 성장**: 걸음수에 따라 거북이가 자라남
- 🏝️ **위치 기반 보상**: 특정 장소 도착 시 아이템 획득
- 💾 **자동 저장**: 진행상황이 자동으로 저장됨

---

## ✨ 주요 기능

### 1. NFC 키링 시스템
- 키링을 휴대폰에 가까이 대면 웹사이트 자동 실행
- 거북이 알 자동 생성
- 재방문 시 이전 진행상황 불러오기

### 2. 러닝 트래킹
- 실시간 GPS 위치 추적
- 지도에 경로 자동 그리기
- 걸음수 및 거리 자동 계산

### 3. 거북이 성장 시스템
| 단계 | 이모지 | 이름 | 필요 걸음수 |
|------|--------|------|-------------|
| 1 | 🥚 | 거북이 알 | 0 |
| 2 | 🐢 | 아기 거북이 | 1,000 |
| 3 | 🐢 | 성체 거북이 | 5,000 |
| 4 | 🐲 | 전설의 거북이 | 10,000 |

### 4. 거북섬 & 아이템
- 거북섬(반경 100m) 도착 시 자동 아이템 지급
- 다양한 아이템 수집
- 아이템 컬렉션 페이지

### 5. 진행상황 관리
- LocalStorage 자동 저장
- 언제든 이어서 플레이
- 초기화 기능

---

## 🚀 빠른 시작

### 필요한 것

- [ ] 스마트폰 (Android 또는 iOS)
- [ ] NFC 키링
- [ ] GitHub 계정 (무료)

### 3단계로 시작하기

#### 1️⃣ 웹사이트 배포 (5분)

```bash
1. GitHub.com 가입
2. New Repository 생성 (이름: turtle-run)
3. index.html 업로드
4. Settings → Pages → Branch: main 선택
5. 완료! (URL: https://[사용자명].github.io/turtle-run/)
```

#### 2️⃣ NFC Tools 설치 (1분)

```bash
Google Play Store → "NFC Tools" 검색 → 설치
```

#### 3️⃣ NFC 키링 설정 (2분)

```bash
1. NFC Tools 실행
2. "쓰기" 탭
3. "레코드 추가" → "URL / URI"
4. 웹사이트 주소 입력
5. "쓰기" 버튼 → 키링 대기
6. 완료!
```

### 🎉 완성!

이제 키링을 휴대폰에 대면 자동으로 게임이 시작됩니다!

---

## 📚 상세 가이드

프로젝트에는 다음 가이드 문서들이 포함되어 있습니다:

### 📄 제공되는 파일

| 파일명 | 설명 | 예상 소요시간 |
|--------|------|----------------|
| **index.html** | 메인 웹사이트 파일 | - |
| **QUICK_START.md** | 5분 빠른 시작 가이드 | 8분 |
| **DEPLOYMENT_GUIDE.md** | 상세 배포 가이드 | 15분 |
| **NFC_SETUP_GUIDE.md** | NFC 설정 완벽 가이드 | 10분 |
| **CUSTOMIZATION_GUIDE.md** | 커스터마이징 가이드 | - |
| **README.md** | 이 문서 | - |

### 📖 읽는 순서

```
처음 시작하는 분:
QUICK_START.md → NFC_SETUP_GUIDE.md → 완료!

더 자세히 알고 싶은 분:
README.md → DEPLOYMENT_GUIDE.md → NFC_SETUP_GUIDE.md → CUSTOMIZATION_GUIDE.md

개발자:
CUSTOMIZATION_GUIDE.md → index.html 코드 분석
```

---

## 🛠️ 기술 스택

### 프론트엔드
- **HTML5** - 웹 구조
- **CSS3** - 스타일링 & 애니메이션
- **JavaScript (ES6+)** - 게임 로직

### APIs & 라이브러리
- **Web NFC API** - NFC 태그 읽기/쓰기
- **Geolocation API** - GPS 위치 추적
- **Leaflet.js** - 인터랙티브 지도
- **OpenStreetMap** - 지도 타일
- **LocalStorage API** - 데이터 저장

### 호스팅
- **GitHub Pages** (권장)
- 또는 Netlify, Vercel, Firebase Hosting

---

## 🎨 커스터마이징

### 거북섬 위치 변경

`index.html`에서 다음 부분을 수정:

```javascript
const TURTLE_ISLAND = {
    lat: 37.4563,  // ← 실제 위도로 변경
    lng: 126.7052, // ← 실제 경도로 변경
    radius: 100    // 반경 (미터)
};
```

### 성장 속도 조절

```javascript
const TURTLE_STAGES = [
    { emoji: '🥚', name: '거북이 알', stepsRequired: 0 },
    { emoji: '🐢', name: '아기 거북이', stepsRequired: 1000 },  // 변경 가능
    { emoji: '🐢', name: '성체 거북이', stepsRequired: 5000 },  // 변경 가능
    { emoji: '🐲', name: '전설의 거북이', stepsRequired: 10000 } // 변경 가능
];
```

### 색상 테마 변경

```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    /* 원하는 색상으로 변경 가능 */
}
```

더 자세한 커스터마이징은 `CUSTOMIZATION_GUIDE.md`를 참고하세요!

---

## ❓ FAQ

### Q1. NFC가 없는 키링도 사용 가능한가요?
**A:** 네! "NFC 없이 시작하기" 버튼을 눌러 바로 게임을 시작할 수 있습니다. 웹사이트를 북마크해서 사용하세요.

### Q2. iPhone에서도 작동하나요?
**A:** 부분적으로 가능합니다.
- NFC 읽기: ✅ (자동 알림으로 웹사이트 열림)
- NFC 쓰기: ⚠️ (제한적, 앱 필요)
- GPS 추적: ✅
- 게임 기능: ✅

### Q3. 오프라인에서도 작동하나요?
**A:** 아니요. 웹사이트 접속과 GPS 사용을 위해 인터넷 연결이 필요합니다.

### Q4. 배터리 소모가 심한가요?
**A:** GPS를 계속 사용하므로 배터리 소모가 있습니다. 러닝 중지 버튼을 누르면 GPS 추적이 멈춥니다.

### Q5. 친구와 함께 사용할 수 있나요?
**A:** 각자의 휴대폰에서 웹사이트에 접속하면 됩니다. 같은 NFC 키링을 여러 사람이 태그해도 각자의 진행상황은 분리됩니다.

### Q6. 데이터는 어디에 저장되나요?
**A:** 휴대폰의 브라우저 LocalStorage에 저장됩니다. 서버에는 전송되지 않으므로 프라이버시가 보호됩니다.

### Q7. 거북섬 위치를 여러 개 만들 수 있나요?
**A:** 네! `CUSTOMIZATION_GUIDE.md`의 "여러 개의 특별한 장소 추가하기" 섹션을 참고하세요.

### Q8. 웹사이트 수정 후 적용이 안돼요.
**A:** 브라우저 캐시를 삭제하거나, 시크릿 모드로 접속해보세요. GitHub Pages는 업데이트 후 5-10분 정도 걸립니다.

---

## 🐛 문제 해결

### NFC 관련

**문제: NFC가 감지되지 않아요**
```
해결책:
✓ 설정 → NFC 켜기
✓ 케이스 제거
✓ 휴대폰 뒷면에 딱 붙이기
✓ 다른 위치에서 시도
```

**문제: URL이 열리지 않아요**
```
해결책:
✓ URL에 https:// 포함 확인
✓ 웹사이트 배포 확인
✓ 10분 대기 후 재시도
```

### GPS 관련

**문제: 위치를 찾을 수 없어요**
```
해결책:
✓ 위치 권한 허용 확인
✓ GPS 켜기
✓ 야외에서 시도 (실내는 GPS 약함)
✓ 비행기 모드 해제
```

**문제: 경로가 엉망으로 그려져요**
```
해결책:
✓ GPS 정확도 "높음"으로 설정
✓ Wi-Fi 켜기 (GPS 보조)
✓ 빌딩 사이가 아닌 열린 공간에서 사용
```

---

## 🎯 로드맵

### 버전 1.0 (현재) ✅
- [x] NFC 키링 연동
- [x] GPS 경로 추적
- [x] 거북이 성장 시스템
- [x] 거북섬 아이템 시스템
- [x] 자동 저장 기능

### 버전 1.1 (계획 중)
- [ ] 일일/주간 목표 설정
- [ ] 친구와 순위 경쟁
- [ ] 업적 시스템
- [ ] 다크 모드
- [ ] 여러 언어 지원

### 버전 2.0 (미래)
- [ ] 실시간 멀티플레이
- [ ] 소셜 기능
- [ ] 거북이 커스터마이징
- [ ] 음악 재생 기능
- [ ] 통계 그래프

---

## 🤝 기여하기

개선 아이디어나 버그 리포트가 있으시면:

1. Issue 생성
2. Pull Request 제출
3. 직접 문의

모든 기여를 환영합니다! 🎉

---

## 📜 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

```
MIT License

Copyright (c) 2024 Turtle Run

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

전체 라이선스는 LICENSE 파일을 참고하세요.

---

## 💌 크레딧

### 사용된 오픈소스

- [Leaflet.js](https://leafletjs.com/) - 지도 라이브러리
- [OpenStreetMap](https://www.openstreetmap.org/) - 지도 데이터
- [NFC Tools](https://www.wakdev.com/en/apps/nfc-tools-android.html) - NFC 앱

### 이모지 출처

모든 이모지는 Unicode 표준 이모지입니다.

---

## 📞 연락처 & 지원

- **Email**: (이메일 주소)
- **GitHub**: (GitHub 프로필)
- **Website**: (웹사이트 주소)

---

## 🎊 감사합니다!

터틀런을 사용해주셔서 감사합니다! 🐢

즐거운 러닝 되세요! 🏃‍♂️💨

---

<div align="center">

Made with ❤️ for runners

[⬆ 맨 위로](#-터틀런-turtle-run---nfc-러닝-게임)

</div>
