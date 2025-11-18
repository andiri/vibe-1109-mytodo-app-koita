# MyToDo 📝

초보 개발자를 위한 심플한 할 일 관리 웹앱입니다.  
바이브코딩 철학에 맞춰 **최소한의 코드로 핵심 기능**을 구현했습니다.

**삼성 One UI 디자인 시스템** 기반으로 제작되어 최신 모바일 디자인 트렌드를 반영했습니다.

![MyToDo 스크린샷](https://via.placeholder.com/500x400/667eea/ffffff?text=MyToDo+App)

---

## ✨ 주요 기능

✅ **할 일 추가** - 텍스트 입력 후 Enter 또는 + 버튼 클릭  
✅ **할 일 수정** - 더블클릭으로 인라인 수정 (Enter로 저장, ESC로 취소)  
✅ **할 일 삭제** - × 버튼으로 개별 삭제  
✅ **완료 체크** - 체크박스로 완료/미완료 토글  
✅ **필터 기능** - 전체/진행중/완료 항목 필터링  
✅ **일괄 삭제** - 완료된 할 일 한 번에 삭제  
✅ **데이터 저장** - localStorage로 새로고침 후에도 유지  
✅ **실시간 통계** - 전체/완료/진행중 개수 자동 업데이트  
✅ **토스트 알림** - 모든 이벤트에 시각적 피드백 메시지  
✅ **다크모드** - 라이트/다크 테마 전환 (자동 저장)  
✅ **반응형 디자인** - 모바일/태블릿/데스크톱 모두 지원  
✅ **One UI 원칙** - 상단은 보기, 하단은 조작  

---

## 🚀 빠른 시작

### 1. 파일 다운로드
```bash
git clone [your-repository-url]
cd mytodo
```

### 2. 실행하기
`index.html` 파일을 브라우저에서 열기만 하면 됩니다!

- **방법 1**: 파일 더블클릭
- **방법 2**: 브라우저에 드래그 앤 드롭
- **방법 3**: 터미널에서 `open index.html` (Mac) 또는 `start index.html` (Windows)

**별도의 설치나 빌드 과정이 필요 없습니다!** 🎉

---

## 📁 프로젝트 구조

```
mytodo/
├── index.html          # 메인 HTML (UI + 기능 구현)
├── style.css           # 스타일시트
└── README.md           # 이 파일
```

**총 3개 파일, 약 430줄의 JavaScript 코드**로 완성된 풀스택 투두 앱!

---

## 🎨 One UI 디자인 특징

이 프로젝트는 [삼성 One UI 디자인 시스템](https://developer.samsung.com/one-ui/index.html)의 핵심 원칙을 따릅니다.

### One UI 4가지 핵심 원칙

1. **Focus on the task at hand** (작업에 집중)
   - 단순하고 직관적인 디자인으로 사용자가 콘텐츠에 집중
   - 빠르고 부드러운 사용자 여정

2. **Interact naturally** (자연스러운 인터랙션)
   - 화면 상단: **Viewing Area** (보기 영역) - 통계와 할 일 리스트
   - 화면 하단: **Interaction Area** (조작 영역) - 입력 필드와 추가 버튼
   - 손이 닿기 쉬운 위치에 버튼 배치

3. **Be visibly comfortable** (시각적 편안함)
   - 다크모드 지원으로 눈의 피로 감소
   - 고대비 색상으로 가독성 향상
   - 적절한 폰트 크기와 여백

4. **Make things responsive** (반응형)
   - 모든 디바이스에 최적화된 레이아웃
   - 최소 터치 영역 64px (접근성)

### 컬러 시스템

**Light Theme**
- Primary: #0078ff (시스템 블루)
- Background: #f6f6f6
- Surface: #ffffff

**Dark Theme**  
- Primary: #0a84ff (밝은 블루)
- Background: #000000
- Surface: #1c1c1e

### UI/UX 포인트
- 🌙 라이트/다크 모드 자동 저장
- 🎯 최소 64px 터치 영역 (One UI 가이드라인)
- 📊 시각적 통계 카드 (호버 효과)
- 🎨 SVG 아이콘으로 선명한 그래픽
- ✨ 부드러운 애니메이션과 트랜지션
- 🎴 일관된 카드 디자인 (테두리, 그림자, 호버)
- 💎 세련된 필터 버튼 스타일

### 반응형 디자인 - 2가지 레이아웃

#### 📱 모바일 & 태블릿 (< 1024px)
```
┌─────────────────────┐
│   MyToDo      🌙    │
│   오늘의 할 일...   │
├─────────────────────┤
│ 전체 │ 완료 │ 진행중 │
│  3  │  1  │   2   │
├─────────────────────┤
│ ☐ 장보기        ×  │
│ ☑ 운동하기      ×  │
│ ☐ 책 읽기       ×  │
├─────────────────────┤
│ [새로운 할 일...][+]│
└─────────────────────┘
```
- **동일한 모바일 레이아웃** (스마트폰 & 태블릿)
- 세로 스크롤, 단일 컬럼
- 입력 영역 하단 고정 (One UI 원칙)
- 컴팩트한 통계 카드 (3개 가로 배치)
- 삭제 버튼 항상 표시
- 태블릿에서는 여백과 그림자 추가

#### 💻 데스크톱 (≥ 1024px) - 2단 레이아웃
```
┌──────────────┬────────────────────────┐
│  MyToDo  🌙  │                        │
│  오늘의...   │                        │
├──────────────┤  ☐ 장보기          ×  │
│  전체     3  │                        │
│  완료     1  │  ☑ 운동하기        ×  │
│  진행중   2  │                        │
├──────────────┤  ☐ 책 읽기         ×  │
│              │                        │
│ ┌──────────┐ │                        │
│ │새할일...│ │                        │
│ └──────────┘ │                        │
│ [새 할 일 +] │                        │
└──────────────┴────────────────────────┘
```
- **왼쪽 사이드바 (380px)**: 헤더 + 통계 + 입력
- **오른쪽 메인 영역**: 할 일 리스트 (넓은 공간)
- 통계 카드 세로 배치, 가로 레이블/값
- 추가 버튼에 텍스트 표시
- 카드 스타일 할 일 항목
- 호버 시 삭제 버튼 표시

---

## 💻 기술 스택

| 기술 | 용도 |
|------|------|
| HTML5 | 시맨틱 마크업, 접근성 (ARIA) |
| CSS3 | CSS Variables, Flexbox, Grid, 다크모드 |
| Vanilla JavaScript | DOM 조작, 이벤트 처리, localStorage, 필터링, 토스트 알림 (370줄) |

**프레임워크 없이 순수 웹 기술만 사용**했습니다.

**주요 특징**:
- 📐 **폰트 크기 25% 증가** - 더 읽기 편한 대형 텍스트
- 📱 **모바일 우선 디자인** - 스마트폰과 태블릿에 동일한 UI
- 💻 **데스크톱 2단 레이아웃** - 공간 효율적 사이드바 구조
- 🎴 **일관된 카드 디자인** - 모든 디바이스에서 통일된 스타일
- 👤 **개발자 정보 푸터** - Made by JUN.VIBE & Cursor

### 디자인 시스템

- **One UI Design System** by Samsung - [공식 문서](https://developer.samsung.com/one-ui/index.html)
  - [Structure](https://developer.samsung.com/one-ui/structure/basic.html)
  - [Color System](https://developer.samsung.com/one-ui/color/system.html)
  - [Theme](https://developer.samsung.com/one-ui/color/theme.html)

---

## 📖 사용 방법

### ➕ 할 일 추가하기
1. 입력 필드에 할 일 입력
2. **Enter** 키 또는 **+** 버튼 클릭
3. 자동으로 localStorage에 저장됨
4. 데스크톱에서는 "새 할 일 추가" 텍스트 버튼으로 표시

### ✏️ 할 일 수정하기 
- 수정할 항목을 **더블클릭**
- 인라인 편집 모드로 전환 (파란색 배경)
- **Enter** 키로 저장 또는 **ESC** 키로 취소
- 포커스를 잃으면 자동 저장

### ✅ 완료 표시하기
- 체크박스 클릭 → 취소선 + 투명도 효과
- 통계가 실시간 자동 업데이트
- localStorage에 상태 자동 저장

### ❌ 할 일 삭제하기
- **개별 삭제**: 항목의 × 버튼 클릭 (슬라이드 아웃 애니메이션)
- **일괄 삭제**: "완료 삭제" 버튼으로 완료된 항목 한 번에 삭제
- 삭제 전 확인 메시지 표시
- 모바일/태블릿에서는 × 버튼 항상 표시

### 🔍 필터 기능
- **전체**: 모든 할 일 표시
- **진행중**: 미완료 항목만 표시
- **완료**: 완료된 항목만 표시
- 필터 변경 시 통계는 전체 데이터 기준 유지

### 🌙 테마 전환하기
- 우측 상단 🌙/☀️ 버튼으로 다크/라이트 모드 전환
- localStorage에 설정 자동 저장

### 📊 통계 확인하기
- 실시간으로 전체/완료/진행중 개수 표시
- 데스크톱에서는 우측 상단에 3개 카드로 표시
- 필터와 무관하게 전체 데이터 통계

### 🎉 토스트 알림 메시지
- 모든 액션에 시각적 피드백 제공
- **성공** (초록색): 할 일 추가, 완료, 일괄 삭제 완료
- **정보** (파란색): 할 일 수정, 완료 취소, 필터 변경
- **경고** (주황색): 빈 입력 경고
- **오류** (빨간색): 할 일 삭제
- 3초 후 자동으로 사라짐
- 슬라이드 인/아웃 애니메이션

---

## 🎯 학습 포인트

이 프로젝트를 통해 배울 수 있는 것들:

### 디자인
1. **One UI 디자인 시스템** - 실무에서 사용되는 디자인 원칙
2. **Viewing/Interaction Area** - 모바일 UX의 핵심 개념
3. **다크모드 구현** - CSS Variables와 data-attribute 활용
4. **접근성** - 터치 영역, ARIA 레이블, 포커스 관리
5. **반응형 디자인** - 2가지 레이아웃 (모바일/태블릿 통합, 데스크톱 별도)
6. **가독성 우선** - 기본 폰트보다 25% 큰 텍스트

### 기술
1. **시맨틱 HTML** - 구조화된 마크업
2. **CSS Variables** - 테마 시스템 구축
3. **CSS Grid & Flexbox** - 복잡한 2단 레이아웃 구현
4. **Media Queries** - 정밀한 반응형 디자인
5. **localStorage API** - 할 일 데이터 영구 저장
6. **DOM 조작** - JavaScript로 동적 렌더링
7. **이벤트 위임** - 효율적인 이벤트 처리
8. **Array 메서드** - filter, find, map 등으로 데이터 관리
9. **ContentEditable API** - 인라인 텍스트 편집
10. **동적 DOM 생성** - 토스트 메시지 시스템
11. **CSS 애니메이션** - keyframes를 이용한 슬라이드 효과

---

## 🔧 커스터마이징

### 색상 변경
`style.css` 파일의 `:root`와 `[data-theme="dark"]` 섹션에서 CSS 변수 값을 변경하세요:

```css
:root {
    --primary: #0078ff;       /* 메인 컬러 */
    --secondary: #5856d6;     /* 보조 컬러 */
    /* ... */
}
```

### 테마 커스터마이징
다크모드 색상도 독립적으로 설정 가능:

```css
[data-theme="dark"] {
    --primary: #0a84ff;
    --background: #000000;
    /* ... */
}
```

### 컨테이너 크기 조정
```css
.container {
    max-width: 600px;  /* 원하는 크기로 변경 */
}
```

### 터치 영역 크기
One UI는 최소 48px 권장, 본 프로젝트는 56px 사용:

```css
.todo-item {
    min-height: 56px;  /* 모바일/태블릿 */
}

/* 데스크톱 */
.todo-item {
    min-height: 80px;
}
```

### 반응형 브레이크포인트 변경
```css
/* 모바일 & 태블릿 */
@media (max-width: 1023px) { ... }

/* 태블릿 추가 여백 */
@media (min-width: 600px) and (max-width: 1023px) { ... }

/* 데스크톱 */
@media (min-width: 1024px) { ... }
```

### 폰트 크기 조정
기본 폰트 크기를 25% 증가:

```css
:root {
    --font-size-xs: 16px;      /* 원래 13px */
    --font-size-sm: 17.5px;    /* 원래 14px */
    --font-size-base: 20px;    /* 원래 16px */
    --font-size-lg: 22.5px;    /* 원래 18px */
    --font-size-xl: 30px;      /* 원래 24px */
    --font-size-2xl: 40px;     /* 원래 32px */
}
```

---

## 🎓 코드 학습 포인트 (입문자용)

### 데이터 저장 (localStorage)
```javascript
// 저장하기
localStorage.setItem('todos', JSON.stringify(todos));

// 불러오기
const saved = localStorage.getItem('todos');
todos = saved ? JSON.parse(saved) : [];
```

### 배열 필터링
```javascript
// 조건에 맞는 항목만 추출
const activeTodos = todos.filter(todo => !todo.completed);
const completedTodos = todos.filter(todo => todo.completed);
```

### 배열에서 특정 항목 찾기
```javascript
// ID로 할 일 찾기
const todo = todos.find(t => t.id === todoId);
```

### 동적 HTML 생성
```javascript
// 템플릿 리터럴로 HTML 생성
li.innerHTML = `
    <input type="checkbox" ${todo.completed ? 'checked' : ''}>
    <span>${todo.text}</span>
`;
```

### 이벤트 위임
```javascript
// 부모 요소에 리스너 하나만 등록
todoList.addEventListener('click', (e) => {
    const item = e.target.closest('.todo-item');
    // 모든 자식 요소의 클릭 처리
});
```

### 토스트 메시지 시스템
```javascript
function showToast(message, type = 'info') {
    const toast = document.createElement('div');
    toast.className = `toast toast-${type}`;
    toast.innerHTML = `
        <span class="toast-icon">${icons[type]}</span>
        <span class="toast-message">${message}</span>
    `;
    toastContainer.appendChild(toast);
    
    // 3초 후 자동 제거
    setTimeout(() => {
        toast.classList.add('toast-hiding');
        setTimeout(() => toast.remove(), 300);
    }, 3000);
}
```

---

## 🌟 추가 개선 아이디어

현재 구현된 기능:
- [x] localStorage 데이터 저장
- [x] 필터 기능 (전체/완료/미완료)
- [x] 할 일 수정 (더블클릭 편집)
- [x] 완료 항목 일괄 삭제

더 발전시키고 싶다면?
- [ ] 드래그 앤 드롭으로 순서 변경
- [ ] 우선순위 설정 (중요도 별 색상/아이콘)
- [ ] 마감일 설정 및 알림
- [ ] 시스템 테마 자동 감지 (`prefers-color-scheme`)
- [ ] 카테고리별 그룹화
- [ ] 검색 기능
- [ ] 정렬 기능 (날짜, 이름, 중요도)
- [ ] PWA 변환 (오프라인 지원)
- [ ] 데이터 내보내기/가져오기 (JSON)
- [ ] 할 일 복사 기능

---

## 🎨 디자인 일관성

### 카드 스타일 (모든 디바이스 공통)
- **테두리**: 1px solid outline
- **그림자**: 기본 `0 2px 4px`, 호버 시 `0 4px 12px`
- **호버 효과**: `translateY(-2px)` + 테두리 색상 primary로 변경
- **배경**: surface-variant
- **둥근 모서리**: 16px (radius-md)

### 적용 요소
- ✅ 통계 카드 (전체/완료/진행중)
- ✅ 할 일 항목 카드
- ✅ 필터 버튼
- ✅ 빈 상태 메시지

---

## 📄 라이선스

MIT License - 자유롭게 사용하세요!

---

## 🙏 크레딧

**개발자**  
**Made by JUN.VIBE & Cursor** 🚀

**바이브코딩 철학** - 최소한의 코드로 최대한의 가치를  
초보 개발자도 쉽게 이해하고 수정할 수 있도록 설계되었습니다.

**디자인 시스템**  
- [Samsung One UI Design System](https://developer.samsung.com/one-ui/index.html) - 삼성전자의 공식 디자인 가이드라인 적용

**참고 자료**
- [One UI - Basic Structure](https://developer.samsung.com/one-ui/structure/basic.html)
- [One UI - Color System](https://developer.samsung.com/one-ui/color/system.html)

---

## 📞 문의

궁금한 점이나 개선 제안이 있다면 Issue를 남겨주세요!

**Happy Coding! 🚀**

