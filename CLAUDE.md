# 씨몬스터(Seamonster) 디자인 시스템

> 이 파일은 Claude Code가 자동으로 읽습니다. 모든 작업에 아래 규칙을 적용하세요.

## 작업 시작 전 필수
- 코드 작성 전 반드시 `git pull` 실행할 것

---

## 브랜드 성격
따뜻하고, 친근하고, 신뢰감 있는 반려동물 사료 쇼핑몰.
카드 기반 UI, 부드러운 모서리, 넉넉한 여백, 오렌지 계열 강조색.

## CSS 변수 (하드코딩 금지, 반드시 변수 사용)

```css
:root {
  /* 컬러 */
  --sm-orange: #F15A30;
  --sm-orange-hover: #D94E26;
  --sm-orange-light: rgba(241,90,48,0.06);
  --sm-orange-border: rgba(241,90,48,0.12);
  --sm-orange-glow: rgba(241,90,48,0.12);
  --sm-black: #1A1A1A;
  --sm-dark: #37352F;
  --sm-white: #FFFFFF;
  --sm-border: #EEEEEE;
  --sm-text-mid: #666666;
  --sm-text-light: #999999;
  --sm-bg: #FAFAFA;
  --sm-bg-warm: #FFF5F0;
  --sm-highlight: #FFF4B3;

  /* 사이징 */
  --sm-container: 720px;
  --sm-container-width: 1320px;
  --sm-side-padding: 20px;
  --sm-pad: 24px;

  /* 라운딩 */
  --sm-radius: 8px;
  --sm-radius-sm: 8px;
  --sm-radius-lg: 12px;
  --sm-radius-card: 16px;
  --sm-radius-btn: 12px;
  --sm-radius-pill: 50px;
  --sm-radius-circle: 50%;

  /* 그림자 */
  --sm-shadow-header: 0 2px 12px rgba(0,0,0,0.06);
  --sm-shadow-card: 0 4px 12px rgba(0,0,0,0.04);
  --sm-shadow-float: 0 10px 30px rgba(0,0,0,0.06);

  /* z-index */
  --sm-z-header: 9999;
  --sm-z-modal: 1000000001;
  --sm-z-toast: 10001;
  --sm-z-float-btn: 1000;
}
```

## 타이포그래피

폰트: "Pretendard Variable", "Pretendard", -apple-system, BlinkMacSystemFont, system-ui, Roboto, "Helvetica Neue", "Segoe UI", "Apple SD Gothic Neo", "Noto Sans KR", sans-serif

| 레벨 | 크기 | 용도 |
|---|---|---|
| Display | 42px | 배너 타이틀 |
| H1 | 32px | 페이지 타이틀 |
| H2 | 28px | 섹션 타이틀 |
| H3 | 22px | 서브 섹션 |
| H4 | 19px | 카드 타이틀 |
| Body L | 17px | 상품명 |
| Body | 15-16px | 기본 본문 |
| Label | 14px | 라벨 |
| Caption | 13px | 캡션 |
| Small | 12px | 뱃지 |

최소 폰트: 13px / 굵기: 400(본문) 500(라벨) 600(카테고리) 700(버튼/가격) 800+(배너)

## 간격 (8px 기반)
4 → 8 → 12 → 16 → 24 → 32 → 48 → 64 → 80 → 120px

## 버튼

**Primary (CTA):** bg var(--sm-orange), color white, radius 50px, font 700 15px
- hover: bg var(--sm-orange-hover), shadow 0 4px 12px rgba(241,90,48,.2)
- disabled: bg #EEE, color #999

**Secondary:** bg white, border 1px solid var(--sm-border), radius 50px
- hover: bg var(--sm-bg-warm), border/color var(--sm-orange)

## 상품 카드
- radius 16px, border 1px solid #EEE, shadow var(--sm-shadow-card)
- 이미지 1:1, hover scale(1.05)
- 카드 hover: border orange, shadow 증가, translateY(-3px)
- 상품명 17px 700 / 가격 15px 700 orange / 별점 13px

## 레이아웃
- 2단: left flex:1 + right 380px sticky
- 그리드: 3열(961px+) → 2열(768-960) → 1열(~767)
- 컨테이너: max-width 1320px, padding 48px 32px

## 반응형
- 모바일 우선, clamp() 활용
- 브레이크: 480 → 767 → 960 → 1024 → 1440px
- .display-m (모바일) / .display-pc (데스크톱)
- 터치 타겟 44px+, @media(hover:hover)

## 트랜지션
- 기본: all 0.2s ease
- 헤더: all 0.4s ease-in-out
- 진행률: width 0.6s cubic-bezier(.25,.46,.45,.94)

## 클래스 네이밍
- sm- (씨몬스터 커스텀), pg- (상품 그리드), xans- (Cafe24 기본)

## 핵심 원칙 (반드시 지킬 것)
1. CTA/강조에 --sm-orange 사용 (하드코딩 금지)
2. 카드 16px radius, 버튼 50px pill
3. 8px 기반 간격, 섹션 간 48-80px
4. 가벼운 그림자 (opacity 0.04-0.06)
5. 0.2s ease 기본 트랜지션
6. 터치 타겟 44px+
7. hover 시 카드 상승 + 오렌지 테두리
8. 최소 폰트 13px, Pretendard Variable
9. 모바일 우선, clamp() 활용
10. 새 컴포넌트 만들기 전 기존 코드 먼저 참조

## 상세 문서
- 전체 매뉴얼: docs/design-system.md
- Claude 프롬프트: docs/claude-prompt.md
