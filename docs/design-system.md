# Seamonster UI/UX Design Manual

> Cafe24 기반 씨몬스터(Seamonster) 공식몰 디자인 시스템 가이드

---

## 1. 브랜드 아이덴티티

### 핵심 키워드
- **따뜻한**, **친근한**, **신뢰감 있는** 반려동물 사료 쇼핑몰
- 카드 기반 UI, 부드러운 모서리, 넉넉한 여백
- 오렌지 계열 강조색으로 활력과 따뜻함 표현

---

## 2. 컬러 시스템

### 2.1 Primary (브랜드)
| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-orange` | `#F15A30` | CTA 버튼, 강조 텍스트, 활성 상태 |
| `--sm-orange-hover` | `#D94E26` | 버튼 hover |
| `--sm-orange-light` | `rgba(241,90,48,0.06)` | 연한 오렌지 배경 |
| `--sm-orange-border` | `rgba(241,90,48,0.12)` | 오렌지 테두리 |
| `--sm-bg-warm` | `#FFF5F0` | 따뜻한 배경 (혜택 배너 등) |
| `--sm-highlight` | `#FFF4B3` | 하이라이트 (노란색) |

### 2.2 Neutral (텍스트 & 배경)
| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-black` | `#1A1A1A` | 본문 텍스트 (최상위) |
| `--sm-dark` | `#37352F` | 보조 다크 텍스트 |
| `#333333` | - | 제목 텍스트 |
| `--sm-text-mid` | `#666666` | 중간 톤 설명 텍스트 |
| `--sm-text-light` | `#999999` | 보조 텍스트, 캡션 |
| `#808080` | - | 상단 메뉴 링크 |
| `--sm-border` | `#EEEEEE` | 기본 테두리 |
| `#E8E8E8` | - | 비활성 구분선 |
| `--sm-bg` | `#FAFAFA` | 페이지 배경 |
| `#F5F5F5` | - | UI 요소 배경 |

### 2.3 External (소셜/특수)
| 이름 | 값 | 용도 |
|---|---|---|
| Kakao | `#FEE500` | 카카오 로그인 |
| Naver | `#1EC800` | 네이버 로그인 |
| Facebook | `#177BF2` | 페이스북 |
| Star Rating | `#FACC15` | 별점 |
| Cart Badge | `#FC4B29` | 장바구니 수량 뱃지 |

---

## 3. 타이포그래피

### 3.1 폰트 패밀리
```css
font-family: "Pretendard Variable", "Pretendard", -apple-system,
  BlinkMacSystemFont, system-ui, Roboto, "Helvetica Neue",
  "Segoe UI", "Apple SD Gothic Neo", "Noto Sans KR", sans-serif;
```

### 3.2 폰트 크기 체계
| 레벨 | 크기 | 용도 |
|---|---|---|
| Display | 42px | 메인 배너 타이틀 |
| H1 | 32px | 페이지 타이틀 |
| H2 | 28px | 섹션 타이틀 |
| H3 | 22px | 서브 섹션 |
| H4 | 19px | 카드 타이틀 |
| Body Large | 17px | 상품명 |
| Body | 15-16px | 기본 본문 |
| Label | 14px | 라벨, 보조 텍스트 |
| Caption | 13px | 캡션, 부가 정보 |
| Small | 12px | 뱃지, 태그 |
| Tiny | 11px | 최소 텍스트 |

> **최소 폰트 크기: 13px** (모바일 가독성 보장)

### 3.3 폰트 굵기
| 값 | 용도 |
|---|---|
| 400 | 일반 본문 |
| 500 | 라벨, 메뉴 링크 |
| 600 | 카테고리 네비게이션, 소제목 |
| 700 | 버튼 텍스트, 가격, 상품명 |
| 800-900 | 배너 타이틀, 강조 헤딩 |

---

## 4. 간격 시스템 (Spacing)

### 8px 기반 간격
| 크기 | 값 | 용도 |
|---|---|---|
| 2xs | 4px | 인라인 마이크로 간격 |
| xs | 8px | 아이콘-텍스트 간격 |
| sm | 12px | 카드 내부 요소 간격 |
| md | 16px | 모바일 좌우 패딩 |
| lg | 24px | 컨테이너 패딩 (`--sm-pad`) |
| xl | 32px | 데스크톱 섹션 패딩 |
| 2xl | 48px | 메인 컨테이너 상단 패딩 |
| 3xl | 64-80px | 섹션 간 간격 |
| 4xl | 100-120px | 페이지 하단 여백 |

### 컨테이너 너비
| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-container` | 720px | 좁은 콘텐츠 (주문서 등) |
| `--sm-container-width` | 1320px | 넓은 레이아웃 |
| `--sm-side-padding` | 20px | 사이드 패딩 |

---

## 5. Border Radius

| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-radius-sm` | 8px | 입력 필드, 작은 요소 |
| `--sm-radius` | 8px | 기본 라운딩 |
| `--sm-radius-lg` | 12px | 중간 카드, 혜택 배너 |
| `--sm-radius-card` | 16px | 상품 카드, 모달 |
| `--sm-radius-btn` | 12px | 사각 버튼 |
| `--sm-radius-pill` | 50px | 알약형 버튼 (CTA) |
| `--sm-radius-circle` | 50% | 원형 (아이콘, 뱃지) |

---

## 6. 그림자 (Shadows)

| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-shadow-header` | `0 2px 12px rgba(0,0,0,0.06)` | 헤더 고정 시 |
| `--sm-shadow-card` | `0 4px 12px rgba(0,0,0,0.04)` | 카드 기본 |
| `--sm-shadow-float` | `0 10px 30px rgba(0,0,0,0.06)` | 모달, 플로팅 요소 |
| 오렌지 글로우 | `0 4px 20px rgba(241,90,48,.08)` | CTA 버튼 hover |
| 카드 hover | `0 8px 24px rgba(0,0,0,0.06)` | 카드 호버 상태 |

---

## 7. 컴포넌트 상세

### 7.1 버튼

#### Primary (CTA)
```css
background: #F15A30;
color: #FFFFFF;
padding: 12px 0;  /* 풀폭 */
border-radius: 50px;
font-weight: 700;
font-size: 15px;
/* hover */
background: #D94E26;
box-shadow: 0 4px 12px rgba(241,90,48,.2);
/* disabled */
background: #EEEEEE;
color: #999999;
```

#### Secondary (Outline)
```css
background: #FFFFFF;
border: 1px solid #EEEEEE;
color: #1A1A1A;
border-radius: 50px;
/* hover */
background: #FFF5F0;
border-color: #F15A30;
color: #F15A30;
```

#### Large CTA (결제)
```css
padding: 16px-18px;
font-size: 16px;
font-weight: 700;
width: 100%;  /* 모바일 풀폭 */
```

#### 소셜 로그인 버튼
- Kakao: `background: #FEE500; color: #000;`
- Naver: `background: #1EC800; color: #FFF;`
- Google: `background: #FFF; border: 1px solid #BCBCBC;`
- Apple: `background: #FFF; border: 1px solid #000;`

### 7.2 상품 카드

```
┌─────────────────────┐
│  ┌─────────────────┐ │  border-radius: 16px
│  │                 │ │  border: 1px solid #EEEEEE
│  │   상품 이미지    │ │  aspect-ratio: 1/1
│  │   (1:1)         │ │
│  └─────────────────┘ │
│                       │
│  ⭐⭐⭐⭐⭐ (4.9)     │  13px, #FACC15
│  상품명               │  17px, 700
│  ₩12,900             │  15px, 700, #F15A30
│  [영양정보 보기]       │  13px, 밑줄
│                       │
│  [  담기  ]           │  Primary 버튼 (pill)
│  [- 1 +]              │  수량 조절 (선택 후)
└─────────────────────┘

/* hover 상태 */
border-color: #F15A30;
box-shadow: 0 8px 24px rgba(0,0,0,0.06);
transform: translateY(-3px);
이미지: scale(1.05), transition 0.4s;
```

### 7.3 수량 조절 (Quantity Control)
```css
border: 1px solid #F15A30;
border-radius: 50px;
height: 46px;
/* 버튼 */
width: 44px; height: 44px;
/* hover */
background: #FFF5F0;
```

### 7.4 헤더

```
┌─────────────────────────────────────────────┐
│ 상단 배너 (검정 #000, h:40px, 흰 텍스트)      │
├─────────────────────────────────────────────┤
│ 로고    [검색] [마이] [장바구니(3)]            │  h: 90px
├─────────────────────────────────────────────┤
│ 구매하기 | 정기배송 | 레시피 | 블로그 | 리뷰    │  h: 65px
│ 16px, 600 weight                             │  border-bottom: 1px solid #efefef
└─────────────────────────────────────────────┘
총 높이: 145px (상단 90px + 하단 65px)
```

**스크롤 동작:**
- 60px 스크롤 → 헤더 고정 (`position: fixed`)
- 아래 스크롤 → 헤더 숨김 (`translateY(-80px)`)
- 위 스크롤 → 헤더 표시

### 7.5 모달

```css
background: #FFFFFF;
border-radius: 16px;
max-width: 440px;
/* 오버레이 */
background: rgba(0,0,0,0.6);
backdrop-filter: blur(4px);
/* 닫기 버튼 */
width: 32px; height: 32px;
border-radius: 50%;
background: white;
position: absolute; top-right;
```

### 7.6 진행률 바 (Progress Bar)
```css
/* 트랙 */
height: 8px;
background: #EDEDED;
border-radius: 100px;
/* 채우기 */
background: #F15A30;
transition: width 0.6s cubic-bezier(.25,.46,.45,.94);
```

### 7.7 혜택 배너 (Benefit Banner)
```css
background: #FFF5F0;
border-radius: 10px;
padding: 14px 16px;
/* 헤더 */
font-size: 12px; color: #F15A30; font-weight: 700;
/* 본문 */
font-size: 13px; color: #666;
```

### 7.8 품절 뱃지
```css
background: rgba(26,26,26,.88);
color: white;
border-radius: 999px;
padding: 0 12px;
height: 28px;
position: absolute; /* 카드 좌상단 */
```

---

## 8. 레이아웃 패턴

### 8.1 2단 레이아웃 (골라담기 페이지)
```
┌──────────────────────────────────────────┐
│                max-width: 1320px          │
│  ┌──────────────────┐  ┌──────────────┐  │
│  │     LEFT         │  │    RIGHT     │  │
│  │   (flex: 1)      │  │ (w: 380px)   │  │
│  │                  │  │  sticky      │  │
│  │  - 배너          │  │  top: 40px   │  │
│  │  - 퀴즈 CTA      │  │              │  │
│  │  - 상품 그리드    │  │  주문 요약    │  │
│  │  - 상세 정보      │  │              │  │
│  │                  │  │              │  │
│  └──────────────────┘  └──────────────┘  │
│         gap: 48px                        │
└──────────────────────────────────────────┘
padding: 48px 32px
```

### 8.2 상품 그리드
| 화면 | 컬럼 | 갭 |
|---|---|---|
| 데스크톱 (961px+) | 3열 | 20px |
| 태블릿 (768-960px) | 2열 | 16px |
| 모바일 (~767px) | 1열 | 12px |

### 8.3 장바구니 추천 그리드
| 화면 | 컬럼 | 갭 |
|---|---|---|
| 데스크톱 | 4열 | 16px |
| 모바일 | 2열 | 12px |

---

## 9. 반응형 디자인

### 9.1 브레이크포인트
| 이름 | 값 | 설명 |
|---|---|---|
| Mobile S | 480px | 소형 모바일 |
| Mobile | 767px | 모바일 기준 |
| Tablet | 960px | 태블릿/데스크톱 경계 |
| Desktop | 1024px | 데스크톱 |
| Wide | 1200px | 넓은 데스크톱 |
| XL | 1440px | 초대형 |

### 9.2 반응형 전략
- **모바일 우선** 접근
- `clamp()` 활용한 유동적 크기 조절
  - 제목: `clamp(22px, 5vw, 32px)`
  - 패딩: `clamp(16px, 4vw, 24px)`
- 모바일 전용 클래스: `.display-m`
- 데스크톱 전용 클래스: `.display-pc`

### 9.3 모바일 특수 요소
- 하단 고정 바 (`#orderFixArea`): 모바일에서만 표시
- safe-area-inset 대응: `env(safe-area-inset-bottom, 0px)`
- 터치 타겟: 최소 44px
- hover 효과 제한: `@media (hover: hover)` 사용

---

## 10. 트랜지션 & 애니메이션

### 10.1 표준 트랜지션
| 용도 | 값 |
|---|---|
| 일반 인터랙션 | `all 0.2s ease` |
| 헤더/배너 | `all 0.4s ease-in-out` |
| 부드러운 변환 | `transform 0.3s cubic-bezier(.4,.4,0,1)` |
| 진행률 바 | `width 0.4s cubic-bezier(.25,.46,.45,.94)` |

### 10.2 키프레임 애니메이션
- `transformIcon` - 페이드 인 (opacity 0→1)
- `transformCategory` - 슬라이드 + 페이드
- `spinner` - 로딩 회전 (360deg)
- `bpop` - 팝인 효과 (scale 0.9→1)

---

## 11. Z-Index 계층

| 토큰 | 값 | 용도 |
|---|---|---|
| `--sm-z-toc` | 998 | 목차 |
| `--sm-z-float-btn` | 1000 | 플로팅 버튼 |
| `--sm-z-header` | 9999 | 헤더 |
| `--sm-z-toast` | 10001 | 토스트 알림 |
| `--sm-z-modal` | 1000000001 | 모달 오버레이 |

---

## 12. Cafe24 플랫폼 연동 참고

### 12.1 이커머스 모듈
- `EC_SHOP_FRONT_NEW_PRODUCT_NORMALACTION` - 일반 상품 모듈
- `EC_PRODUCT_ACTION_BASKET` - 장바구니 추가 이벤트
- `SHOP_PRICE_FORMAT.toShopPrice()` - 가격 포맷팅
- `aBasketProductData[]` - 장바구니 데이터 배열

### 12.2 클래스 네이밍 규칙
- `sm-` 접두사: 씨몬스터 커스텀 스타일
- `pg-` 접두사: 상품 그리드 관련
- `xans-` 접두사: Cafe24 기본 모듈
- BEM 변형: `.pg-card`, `.pg-card .pg-body`, `.pg-card .pg-img`

---

## 13. 디자인 원칙 요약

1. **따뜻한 오렌지**: 모든 CTA와 강조에 `#F15A30` 사용
2. **부드러운 모서리**: 카드 16px, 버튼 50px pill 형태
3. **넉넉한 여백**: 섹션 간 48-80px, 8px 기반 간격 체계
4. **가벼운 그림자**: 최소한의 그림자로 깊이감 표현
5. **부드러운 전환**: 0.2-0.4s ease 트랜지션
6. **모바일 우선**: 터치 친화적, 44px 최소 타겟
7. **카드 기반 UI**: hover 시 상승 + 테두리 강조 효과
8. **고대비 텍스트**: `#1A1A1A` on white, `#FFF` on orange
