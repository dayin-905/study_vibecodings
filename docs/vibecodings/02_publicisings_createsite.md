## 작성 프롬프트
### 1차 json 프롬프트 작성
```
너는 20년차 웹 디자이너로 디자인의 영혼을 담아 웹 표준 기반의 섬세하고 생동감 있는 인터랙션을 구현하고, 기술적 완성도를 통해 디자인 비전이 사용자 경험(UX)으로 완벽하게 승화되도록 하는 고도의 전문가야.
해당하는 웹 페이지를 밝고 명량한 느낌으로 재해석하고 싶어.

베이커리 홈페이지를 하나 만들어서 점진적으로 고도화 시키려고 해.
기본적으로 들어가야 할 메뉴탭 구성은 아래를 참고해주고 해당 사이트를 아주 분위기 있고 빈티지 하게 만들고 싶어.

[작업 사항]
1. 메뉴 이름은 모두 영어로 간략하게 작성해주는 메뉴 구성 리스트를 제작.
2. 초기 와이어프레임+빈티지 컨셉에 맞는 구체적인 웹 폰트 추천.
3. 모든 형식은 json 형식의 프롬프트로 작성.
4. [추가 참고 사항] 또한 json 형식 프롬프트에 같이 작성.

[기본 메뉴 구성 리스트]
베이커리 맛집 추천
- 매장 별 메뉴 추천

레시피 공유
- 아침 식사 대용
- 달콤한 디저트
- 식사빵

일상 블로그
- 달력 형태로 되어 누르면 해당 일상 글로 들어가지는 하이퍼 링크 기능

[추가 참고 사항]
메인 화면 - 레이아웃 참고
https://startbootstrap.com/previews/modern-business

관리자 화면 - CRUD(메뉴 구성에 추가)
https://startbootstrap.com/previews/modern-business

레시피 추천 - 레이아웃 참고
https://startbootstrap.com/previews/shop-homepage
```
### json 프롬프트 작성 결과
```
{
  "project_name": "빈티지 베이커리 홈페이지 통합 고도화 계획 (Food Mark)",
  "concept": {
    "style": "빈티지 & 클래식 (Vintage & Classic)",
    "mood": "분위기 있고, 아늑하며, 아날로그 감성",
    "target_audience": "20대 후반 ~ 30대 (감성적인 디지털 콘텐츠 소비자)"
  },
  "color_palette": {
    "primary_base": "#FAFAD2",
    "primary_point": "#3CAEFF",
    "secondary_accent": "#A2E9FF",
    "text_color": "#000000",
    "vintage_tone_note": "톤 다운된 크림색, 베이지, 브라운 계열의 보조색 활용 권장"
  },
  "typography_guide": {
    "main_title_logo": {
      "style": "클래식 세리프 (Classic Serif)",
      "recommendation": ["Playfair Display", "Cormorant Garamond"]
    },
    "body_content_menu": {
      "style": "깨끗한 산세리프 / 세리프 혼용",
      "recommendation": ["Lora", "Inter", "Noto Sans KR (한글)"]
    },
    "accent_signature": {
      "style": "스크립트 (Script) / 손글씨",
      "recommendation": ["Great Vibes", "Caveat"]
    },
    "note": "메인 타이포그래피는 대문자(UPPERCASE) 사용을 권장하여 클래식한 느낌 강조."
  },
  "menu_structure": {
    "menu_system_name": "빈티지 베이커리 홈페이지 메뉴 구성 (관리자 기능 포함)",
    "main_navigation": [
      {
        "korean_name": "베이커리 맛집 추천",
        "english_name": "Our Bakeries",
        "layout_reference": "https://startbootstrap.com/previews/modern-business",
        "sub_menus": [
          {
            "korean_name": "매장 별 메뉴 추천",
            "english_name": "Signature Items",
            "description": "각 매장의 대표 메뉴를 우아하게 지칭"
          }
        ]
      },
      {
        "korean_name": "레시피 공유",
        "english_name": "Recipes",
        "layout_reference": "https://startbootstrap.com/previews/shop-homepage",
        "sub_menus": [
          {
            "korean_name": "아침 식사 대용",
            "english_name": "Morning Loaves",
            "description": "아침용 빵의 따뜻한 감성 표현"
          },
          {
            "korean_name": "달콤한 디저트",
            "english_name": "Sweet Delights",
            "description": "디저트의 감성적이고 우아한 표현"
          }
          ,
          {
            "korean_name": "식사빵",
            "english_name": "Daily Bread",
            "description": "일상적이고 클래식한 식사빵의 느낌 강조"
          }
        ]
      },
      {
        "korean_name": "일상 블로그 & 관리",
        "english_name": "Journal & Admin",
        "sub_menus": [
          {
            "korean_name": "달력 형태 일상 글",
            "english_name": "Archive Calendar",
            "description": "기록 보관소로서의 역할을 강조하여 아날로그적인 빈티지 느낌 부여"
          },
          {
            "korean_name": "관리자 화면 (CRUD)",
            "english_name": "Admin Dashboard (CRUD)",
            "layout_reference": "https://startbootstrap.com/previews/modern-business",
            "description": "콘텐츠 생성/읽기/업데이트/삭제를 위한 관리자 페이지"
          }
        ]
      }
    ]
  },
  "layout_wireframe_details": {
    "header": {
      "logo_placement": "좌측 상단, 여백 강조",
      "nav_style": "중앙 또는 우측 상단, 간결한 대문자 사용",
      "utility": "우측 끝, 최소한의 단색 아이콘 배치 (검색, 장바구니)"
    },
    "hero_section": {
      "visual": "화면 전체를 덮는 고품질 빈티지 필터 이미지/영상",
      "text": "중앙 배치, 감성적인 짧은 문구 (세리프)",
      "cta": "둥근 버튼, 톤 다운된 컬러, 부드러운 호버 애니메이션",
      "layout_reference": "https://startbootstrap.com/previews/modern-business"
    },
    "content_areas": {
      "recipes": "이미지 중심의 3열 카드 레이아웃, 카드에 스크립트 폰트 제목 사용",
      "journal": "달력 형태의 아날로그적인 레이아웃 (Archive Calendar)을 핵심 기능으로 강조"
    },
    "footer": {
      "style": "차분한 베이지색 배경, 작은 폰트, 클래식한 신문 지면 느낌 연출",
      "content": "연락처, 주소, 영업시간, 단색 소셜 미디어 아이콘"
    }
  },
  "design_focus": "단순한 정보 제공을 넘어, 빈티지한 타이포그래피와 여백의 미를 활용하여 '디자인 비전이 사용자 경험으로 승화'되도록 구현"
}
```

## json 프롬프트 작성 결과
