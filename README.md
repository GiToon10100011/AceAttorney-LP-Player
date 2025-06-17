# 🎵 Ace Attorney LP Player

![Ace Attorney LP Player](https://aalpplayer.web.app/images/AA1.jpg)

## 📋 프로젝트 정보

- **개발 기간**: 2024.10 ~ 2024.11
- **개발자**: 전진우
- **배포 주소**: [https://aalpplayer.web.app](https://aalpplayer.web.app)

## 📋 프로젝트 소개

이 프로젝트는 인기 게임 시리즈 '역전재판'의 음악을 LP 레코드 플레이어 형태로 감상할 수 있는 인터랙티브 웹 애플리케이션입니다. 사용자는 회전하는 LP 디스크를 통해 게임 시리즈의 다양한 배경음악을 감상하고, 오디오 시각화 효과를 즐길 수 있습니다.

## 🛠️ 사용 기술

![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Styled Components](https://img.shields.io/badge/Styled_Components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-0055FF?style=for-the-badge&logo=framer&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Web Audio API](https://img.shields.io/badge/Web_Audio_API-FF3E00?style=for-the-badge&logo=webmoney&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)

## ✨ 주요 기능

### 1. LP 레코드 플레이어 인터페이스
사용자는 실제 LP 레코드 플레이어와 유사한 인터페이스를 통해 음악을 재생할 수 있습니다. 재생 시 LP 디스크가 회전하며 실제 레코드 플레이어의 경험을 제공합니다.

### 2. 오디오 시각화
Web Audio API를 활용한 원형 오디오 시각화 기능을 통해 음악의 주파수와 진폭에 따라 변화하는 시각적 효과를 제공합니다.

```typescript
const drawVisualizer = () => {
  // 오디오 데이터 분석
  analyser.getByteFrequencyData(dataArray);
  
  // 원형 시각화 렌더링
  for (let i = 0; i < bufferLength; i++) {
    const value = dataArray[i];
    // 시각화 로직
  }
  
  requestAnimationFrame(drawVisualizer);
};
```

### 3. 회전 메뉴 시스템
원형 메뉴를 통해 다양한 에이스 어토니 시리즈의 음악을 선택할 수 있습니다. 마우스 휠을 사용하여 메뉴를 회전시키고 원하는 트랙을 선택할 수 있습니다.

### 4. RPM 조절 기능
실제 LP 레코드처럼 33RPM과 45RPM 사이의 재생 속도를 전환할 수 있습니다. 이를 통해 음악의 재생 속도를 조절할 수 있습니다.

### 5. 키보드 컨트롤
키보드 방향키와 스페이스바를 사용하여 트랙 이동 및 재생/일시정지를 제어할 수 있습니다.

## 🎮 사용 방법

1. **트랙 선택**: 메뉴 버튼을 클릭하여 회전 메뉴를 열고, 원하는 트랙을 선택합니다.
2. **재생/일시정지**: LP 디스크 중앙의 재생 버튼을 클릭하거나 스페이스바를 누릅니다.
3. **트랙 이동**: 화면 하단의 Prev/Next 버튼이나 키보드 방향키를 사용합니다.
4. **재생 속도 조절**: RPM 스위치를 클릭하여 33RPM과 45RPM 사이를 전환합니다.

## 📂 프로젝트 아키텍처

### 폴더 구조

```
AceAttorney-LP-Player/
├── public/               # 정적 파일
│   ├── images/           # 이미지 파일
│   ├── audio/            # 오디오 파일
│   └── favicon.ico       # 파비콘
├── src/
│   ├── components/       # 리액트 컴포넌트
│   ├── contexts/         # 리액트 컨텍스트
│   │   └── AudioContext.tsx # 오디오 상태 관리 컨텍스트
│   ├── types/            # 타입스크립트 타입 정의
│   ├── utils/            # 유틸리티 함수
│   ├── data/             # 트랙 데이터
│   ├── styles/           # 전역 스타일
│   ├── App.tsx           # 메인 앱 컴포넌트
│   └── index.tsx         # 앱 진입점
└── firebase.json         # Firebase 설정
```

## 🚀 설치 및 실행 방법

1. 저장소를 클론합니다:
   ```
   git clone https://github.com/GiToon10100011/AceAttorney-LP-Player.git
   ```
2. 프로젝트 폴더로 이동합니다:
   ```
   cd AceAttorney-LP-Player
   ```
3. 의존성 패키지를 설치합니다:
   ```
   npm install
   ```
4. 개발 서버를 실행합니다:
   ```
   npm run dev
   ```
5. 빌드 및 배포:
   ```
   npm run deploy
   ```

## 💡 배운 점

### 기술적 측면

- **Web Audio API 활용**: 오디오 컨텍스트와 분석기 노드를 사용하여 실시간 오디오 시각화를 구현하는 방법을 배웠습니다.
- **React와 TypeScript 통합**: TypeScript를 사용하여 타입 안정성이 보장된 React 컴포넌트를 작성하는 방법을 익혔습니다.
- **Framer Motion 애니메이션**: 복잡한 UI 애니메이션을 선언적으로 구현하는 방법을 학습했습니다.
- **오디오 처리**: 오디오 재생 속도 조절 및 이펙트 적용 방법을 연구했습니다.

### 디자인 측면

- **스큐어모픽 디자인**: 실제 물리적 오브젝트를 디지털 인터페이스로 변환하는 디자인 방법론을 적용했습니다.
- **인터랙티브 UI**: 사용자 입력에 즉각적으로 반응하는 인터랙티브 UI 설계 방법을 익혔습니다.
- **시각적 피드백**: 사용자 액션에 대한 적절한 시각적 피드백을 제공하는 방법을 배웠습니다.

## ⚠️ 면책 조항

이 프로젝트는 팬이 제작한 비공식 애플리케이션입니다. '역전재판' 시리즈와 관련된 모든 음악, 이미지, 캐릭터의 저작권은 CAPCOM에 있습니다.
