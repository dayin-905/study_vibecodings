## 프롬프트 작성 시 주의사항 및 회고
- 색상 코드는 해당 사이트를 활용함. (https://www.makeshop.co.kr/newmakeshop/home/faq_view.html?uid=1128)
- 컬러는 3가지를 사용 (1) 기본 컬러 (2) 포인트 컬러 (3) 세컨드 컬러
- 다크 모드에서 가독성이 좋은 20~30대의 혼밥러를 소비자로 설정
- 선생님 조언으로 @를 사용하여 변경할 파일 경로 설정
- 

## 작성 프롬프트
```
너는 20년차 웹 디자이너로 디자인의 영혼을 담아 웹 표준 기반의 섬세하고 생동감 있는 인터랙션을 구현하고, 기술적 완성도를 통해 디자인 비전이 사용자 경험(UX)으로 완벽하게 승화되도록 하는 고도의 전문가야.

해당하는 웹 페이지를 밝고 명량한 느낌으로 재해석하고 싶어.

## 출력 사항
- 해당하는 html 파일만 수정하여 html 파일로 출력한다.

## 원하는 컨셉 방향
- 한 눈에 보기 좋을 수 있도록 가독성을 극대화 한다.
- 기본적으로 사용할 코드 컬러 #FAFAD2 / 포인트 컬러 #3CAEFF / 세컨드 컬러 #A2E9FF를 사용하여 꾸며준다.
- 글자 컬러는 검정색으로 사용해주고 이외의 것들은 유동적으로 디자인 가능하다.
- 대상은 25년도 20~30대 사람의 취향을 고려한다. 

## 제안 사항
- 기존 메뉴는 반드시 유지한다.
- 하위 메뉴 변환은 절대적으로 하지 않는다.

## 변경 html 파일 경로
@파일 경로 설정
```

## 프롬프트 결과(html)
```
<!DOCTYPE html>
<html lang="ko">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Food Mark - 혼밥 레시피 🥄</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="css/style.css" rel="stylesheet"> 

    <style>
        /* 컬러 팔레트 정의 */
        :root {
            --color-base: #FAFAD2; /* 기본 배경색 (Light Goldenrod Yellow) */
            --color-point: #3CAEFF; /* 포인트 컬러 (밝은 파랑/하늘색) */
            --color-secondary: #A2E9FF; /* 세컨드 컬러 (매우 밝은 청록색) */
            --color-text: #000000; /* 글자 컬러 (검정) */
            --font-family-main: 'Spoqa Han Sans Neo', 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        }

        body {
            background-color: var(--color-base); /* 기본 배경색 적용 */
            color: var(--color-text);
            font-family: var(--font-family-main);
        }

        /* 1. 네비게이션 바 스타일 */
        .navbar {
            background-color: var(--color-secondary) !important; /* 세컨드 컬러 적용 */
            font-weight: 600;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* 입체감 부여 */
        }

        .navbar-brand {
            color: var(--color-text) !important;
            font-weight: 800;
            font-size: 1.5rem;
        }
        
        /* 2. 메인 Jumbotron (Hero Section) 스타일 */
        .jumbotron-custom {
            background-color: var(--color-point); /* 포인트 컬러 적용 */
            color: white;
            padding: 5rem 3rem !important; /* 내부 패딩 강화 */
            border-radius: 1.5rem !important; /* 둥근 모서리 강조 */
            box-shadow: 0 8px 15px rgba(60, 174, 255, 0.4); /* 산뜻한 그림자 효과 */
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2); /* 텍스트 가독성 향상 */
        }

        .jumbotron-custom .display-4 {
            font-weight: 900;
        }

        /* 3. 버튼 스타일 */
        .btn-primary {
            background-color: var(--color-point);
            border-color: var(--color-point);
            font-weight: 600;
            transition: background-color 0.3s, transform 0.2s;
        }

        .btn-primary:hover {
            background-color: #3095E7; /* 포인트 컬러보다 약간 진하게 */
            border-color: #3095E7;
            transform: translateY(-2px); /* 약간 띄우는 인터랙션 */
        }

        .btn-outline-success { /* 검색 버튼 스타일 */
            color: var(--color-point);
            border-color: var(--color-point);
            transition: all 0.3s;
        }

        .btn-outline-success:hover {
            background-color: var(--color-point);
            color: white;
        }

        /* 4. 카드 스타일 (가독성 및 산뜻함 강조) */
        .card {
            border: 2px solid var(--color-secondary); /* 세컨드 컬러로 테두리 강조 */
            border-radius: 1rem;
            transition: transform 0.3s, box-shadow 0.3s;
            overflow: hidden; /* 이미지 경계 처리 */
            background-color: white; /* 카드 배경 흰색으로 가독성 확보 */
        }

        .card:hover {
            transform: translateY(-5px); /* 호버 인터랙션 */
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .card-img-top {
            height: 200px; /* 이미지 높이 통일 */
            object-fit: cover;
        }

        .card-body {
            padding: 1.5rem;
        }

        .card-title {
            color: var(--color-point); /* 타이틀에 포인트 컬러 적용 */
            font-weight: 700;
        }

        /* 5. 푸터 스타일 */
        footer {
            background-color: var(--color-secondary); /* 세컨드 컬러 적용 */
            color: var(--color-text);
            margin-top: 4rem !important;
        }

        footer .text-center {
            background-color: rgba(0, 0, 0, 0.1); /* 하단 카피라이트 배경 */
        }
    </style>
</head>

<body>
    <nav class="navbar navbar-expand-lg navbar-light">
        <div class="container-fluid">
            <a class="navbar-brand" href="index.html">Food Mark 🍽️</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <a class="nav-link active" aria-current="page" href="index.html" style="color: var(--color-point) !important; font-weight: 700;">✨ 홈</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="recipes.html" style="color: var(--color-text);">레시피</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="ingredients.html" style="color: var(--color-text);">식재료</a>
                    </li>
                </ul>
                <form class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="궁금한 레시피 검색" aria-label="Search" style="border: 1px solid var(--color-point);">
                    <button class="btn btn-outline-success" type="submit">검색</button>
                </form>
            </div>
        </div>
    </nav>

    <main class="container my-5">
        <section class="jumbotron-custom text-center mb-5">
            <h1 class="display-4 text-white">🍚 혼밥족을 위한 간편 레시피</h1>
            <p class="lead text-white">혼자서도 맛있고 건강하게! <span style="font-weight: 700;">Food Mark</span>가 제안하는 트렌디한 초간단 레시피를 만나보세요.</p>
            <a href="recipes.html" class="btn btn-primary btn-lg mt-3">오늘의 추천 레시피 보기 ➡️</a>
        </section>

        <section class="mb-5">
            <h2 class="text-center mb-4" style="color: var(--color-point); font-weight: 800;">✨ 인기 레시피 Best 3</h2>
            <div class="row">
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <img src="https://via.placeholder.com/400x200/3CAEFF/FFFFFF?text=Kimchi+Jjigae" class="card-img-top" alt="김치찌개">
                        <div class="card-body">
                            <h5 class="card-title">돼지고기 김치찌개 🥘</h5>
                            <p class="card-text">한국인의 소울푸드, 김치찌개를 15분 만에 만드는 비법! 자취생 특화 레시피.</p>
                            <a href="recipe-detail.html" class="btn btn-primary">레시피 보기</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <img src="https://via.placeholder.com/400x200/A2E9FF/000000?text=Ganjang+Gyeranbap" class="card-img-top" alt="계란밥">
                        <div class="card-body">
                            <h5 class="card-title">간장 계란밥 🍳</h5>
                            <p class="card-text">바쁜 아침, 5분이면 완성되는 마약 간장 계란밥! 실패 없는 황금 비율.</p>
                            <a href="recipe-detail.html" class="btn btn-primary">레시피 보기</a>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="card h-100">
                        <img src="https://via.placeholder.com/400x200/FAFAD2/000000?text=Alio+Olio" class="card-img-top" alt="파스타">
                        <div class="card-body">
                            <h5 class="card-title">알리오 올리오 🍝</h5>
                            <p class="card-text">냉장고 속 재료로 뚝딱! 레스토랑 부럽지 않은 나만의 홈 메이드 파스타.</p>
                            <a href="recipe-detail.html" class="btn btn-primary">레시피 보기</a>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="text-center text-lg-start mt-auto">
        <div class="container p-4">
            <div class="row">
                <div class="col-lg-6 col-md-12 mb-4 mb-md-0">
                    <h5 class="text-uppercase" style="font-weight: 700;">Food Mark</h5>
                    <p>
                        Food Mark는 **2030 싱글 라이프**를 위한 쉽고 맛있고, **보기에도 예쁜** 레시피를 제공합니다.
                    </p>
                </div>
            </div>
        </div>
        <div class="text-center p-3">
            © 2025 Food Mark. All rights reserved. 💖
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="js/script.js"></script> 
</body>

</html>
```