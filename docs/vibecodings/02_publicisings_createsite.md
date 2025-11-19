## 프롬프트 작성 시 요청 사항
- 

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
### 추가 입력 사항
#### 1차
```
out signature creations에 들어있는 레시피는 전부 다 지워주고 베이커리 메뉴로 다시 채우기.
들어갈 베이커리 메뉴는 (1) 크로아상 (2) 두바이 쫀득쿠키 (3) 에그타르트 그 안에 레시피는 너가 직접 제작.
contact us에 들어가는 건 주소와 번호는 그대로 두고 이메일에 dayin.9905@gmail.com으로 다시 넣어줘.
그리고 반응형 웹사이트 재제작 요청.
빈티지 베이커리 헤더에 빈티지한 이미지 하나 삽입(안 됐음.)
```
#### 2차
```
관리자 화면 - CRUD(메뉴 구성에 추가) https://startbootstrap.com/previews/modern-business admin 페이지를 눌렀을 때 들어갈 수 있는 페이지로 재제작 요청.
사용 기술 스팩 : HTML, BS5, JS 만 사용해서 추가적으로 제작 요청.
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
```
<!DOCTYPE html>
<html lang="ko">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vintage Bakery - Admin Dashboard</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Lora:wght@400;700&family=Great+Vibes&family=Noto+Sans+KR:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="css/style.css" rel="stylesheet">

    <style>
        /* Inherit from main style for consistency */
        :root {
            --color-base: #FAFAD2;
            --color-point: #3CAEFF;
            --color-secondary: #E0D8B0;
            --color-text: #333333;
            --color-dark-text: #000000;
            --font-family-main: 'Lora', 'Noto Sans KR', serif;
            --font-family-heading: 'Playfair Display', serif;
            --font-family-accent: 'Great Vibes', cursive;
        }

        body {
            background-color: var(--color-base);
            color: var(--color-text);
            font-family: var(--font-family-main);
            line-height: 1.8;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        .navbar {
            background-color: var(--color-base) !important;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }

        .navbar-brand {
            color: var(--color-dark-text) !important;
            font-family: var(--font-family-heading) !important;
            font-weight: 700;
            font-size: 2rem;
            letter-spacing: 1px;
        }

        .sidebar {
            background-color: var(--color-secondary);
            padding: 1rem;
            min-height: calc(100vh - 56px); /* Adjust based on navbar height */
        }

        .sidebar .nav-link {
            color: var(--color-dark-text);
            padding: 0.75rem 1rem;
            border-radius: 0.5rem;
            margin-bottom: 0.5rem;
        }

        .sidebar .nav-link.active,
        .sidebar .nav-link:hover {
            background-color: var(--color-point);
            color: white;
        }

        .admin-card {
            background-color: white;
            border-radius: 1rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            padding: 2rem;
        }

        .btn-primary-admin {
            background-color: var(--color-point);
            border-color: var(--color-point);
            color: white;
        }
        .btn-primary-admin:hover {
            background-color: #3095E7;
            border-color: #3095E7;
        }

        .btn-secondary-admin {
            background-color: var(--color-secondary);
            border-color: var(--color-secondary);
            color: var(--color-dark-text);
        }
        .btn-secondary-admin:hover {
            background-color: #C0B890;
            border-color: #C0B890;
        }

        footer {
            background-color: var(--color-secondary);
            color: var(--color-text);
            padding-top: 3rem;
            margin-top: auto;
        }
    </style>
</head>

<body>
    <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container-fluid">
            <a class="navbar-brand text-uppercase" href="bakery.html">Vintage Bakery Admin</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#adminNavbar"
                aria-controls="adminNavbar" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="adminNavbar">
                <ul class="navbar-nav ms-auto mb-2 mb-lg-0 text-uppercase">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="admin.html">Dashboard</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="bakery.html">Back to Main Site</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>

    <div class="container-fluid">
        <div class="row">
            <!-- Sidebar -->
            <nav id="sidebarMenu" class="col-md-3 col-lg-2 d-md-block sidebar collapse">
                <div class="position-sticky pt-3">
                    <ul class="nav flex-column">
                        <li class="nav-item">
                            <a class="nav-link active" aria-current="page" href="#">
                                <i class="fas fa-home me-2"></i>
                                Overview
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">
                                <i class="fas fa-cookie-bite me-2"></i>
                                Products
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">
                                <i class="fas fa-users me-2"></i>
                                Users
                            </a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">
                                <i class="fas fa-blog me-2"></i>
                                Blog Posts
                            </a>
                        </li>
                    </ul>
                </div>
            </nav>

            <!-- Main Content -->
            <main class="col-md-9 ms-sm-auto col-lg-10 px-md-4">
                <div class="d-flex justify-content-between flex-wrap flex-md-nowrap align-items-center pt-3 pb-2 mb-3 border-bottom">
                    <h1 class="h2" style="font-family: var(--font-family-heading);">Product Management</h1>
                </div>

                <div class="admin-card mb-4">
                    <h3 class="mb-4" style="font-family: var(--font-family-heading);">Add/Edit Product</h3>
                    <form id="productForm">
                        <input type="hidden" id="productId">
                        <div class="mb-3">
                            <label for="productName" class="form-label">Product Name</label>
                            <input type="text" class="form-control" id="productName" required>
                        </div>
                        <div class="mb-3">
                            <label for="productDescription" class="form-label">Description</label>
                            <textarea class="form-control" id="productDescription" rows="3" required></textarea>
                        </div>
                        <div class="mb-3">
                            <label for="productImage" class="form-label">Image URL</label>
                            <input type="url" class="form-control" id="productImage" required>
                        </div>
                        <button type="submit" class="btn btn-primary-admin me-2">Save Product</button>
                        <button type="button" class="btn btn-secondary-admin" id="clearForm">Clear</button>
                    </form>
                </div>

                <div class="admin-card">
                    <h3 class="mb-4" style="font-family: var(--font-family-heading);">Current Products</h3>
                    <div class="table-responsive">
                        <table class="table table-striped table-hover">
                            <thead>
                                <tr>
                                    <th>ID</th>
                                    <th>Name</th>
                                    <th>Description</th>
                                    <th>Image</th>
                                    <th>Actions</th>
                                </tr>
                            </thead>
                            <tbody id="productList">
                                <!-- Product rows will be inserted here by JavaScript -->
                            </tbody>
                        </table>
                    </div>
                </div>
            </main>
        </div>
    </div>

    <footer class="text-center text-lg-start mt-5" style="background-color: var(--color-secondary); color: var(--color-text); font-family: var(--font-family-main);">
        <div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.05); font-size: 0.85rem;">
            © 2025 Vintage Bakery Admin. All rights reserved.
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const productForm = document.getElementById('productForm');
            const productIdInput = document.getElementById('productId');
            const productNameInput = document.getElementById('productName');
            const productDescriptionInput = document.getElementById('productDescription');
            const productImageInput = document.getElementById('productImage');
            const productList = document.getElementById('productList');
            const clearFormButton = document.getElementById('clearForm');

            let products = JSON.parse(localStorage.getItem('adminProducts')) || [];
            let currentId = products.length > 0 ? Math.max(...products.map(p => p.id)) + 1 : 1;

            function renderProducts() {
                productList.innerHTML = '';
                products.forEach(product => {
                    const row = productList.insertRow();
                    row.innerHTML = `
                        <td>${product.id}</td>
                        <td>${product.name}</td>
                        <td>${product.description}</td>
                        <td><img src="${product.image}" alt="${product.name}" style="width: 50px; height: 50px; object-fit: cover; border-radius: 5px;"></td>
                        <td>
                            <button class="btn btn-sm btn-primary-admin edit-btn" data-id="${product.id}">Edit</button>
                            <button class="btn btn-sm btn-danger delete-btn" data-id="${product.id}">Delete</button>
                        </td>
                    `;
                });
                localStorage.setItem('adminProducts', JSON.stringify(products));
            }

            function clearForm() {
                productIdInput.value = '';
                productNameInput.value = '';
                productDescriptionInput.value = '';
                productImageInput.value = '';
            }

            productForm.addEventListener('submit', (e) => {
                e.preventDefault();
                const id = productIdInput.value;
                const name = productNameInput.value;
                const description = productDescriptionInput.value;
                const image = productImageInput.value;

                if (id) {
                    // Update existing product
                    const index = products.findIndex(p => p.id == id);
                    if (index !== -1) {
                        products[index] = { id: parseInt(id), name, description, image };
                    }
                } else {
                    // Add new product
                    products.push({ id: currentId++, name, description, image });
                }
                clearForm();
                renderProducts();
            });

            productList.addEventListener('click', (e) => {
                if (e.target.classList.contains('edit-btn')) {
                    const id = e.target.dataset.id;
                    const product = products.find(p => p.id == id);
                    if (product) {
                        productIdInput.value = product.id;
                        productNameInput.value = product.name;
                        productDescriptionInput.value = product.description;
                        productImageInput.value = product.image;
                    }
                } else if (e.target.classList.contains('delete-btn')) {
                    const id = e.target.dataset.id;
                    products = products.filter(p => p.id != id);
                    renderProducts();
                }
            });

            clearFormButton.addEventListener('click', clearForm);

            renderProducts(); // Initial render
        });
    </script>
</body>

</html>
```