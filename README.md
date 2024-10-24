<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الصفحة الرئيسية</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>

<header>
    <div class="logo">
        <h1><?php echo "moz"; ?></h1>
        <img src="file:///storage/emulated/0/smart shopping/img/smart_shopping.png" alt="Logo" loading="lazy">
    </div>
    
    <div class="search">
        <form action="#" method="get">
            <input type="text" class="search_input" name="search" placeholder="ادخل كلمه البحث" required>
            <button class="button_search" name="btn_search">بحث</button>
        </form>
    </div>

    <div class="settings">
        <button class="settings-toggle" onclick="toggleSettings()" aria-label="إعدادات">⚙️</button>
        <button class="language-toggle" onclick="toggleLanguage()" aria-label="تغيير اللغة">🌐</button>
    </div>
</header>

<nav>
    <div class="social">
        <ul>
            <li><a href="#" target="_blank">فيسبوك</a></li>
            <li><a href="#" target="_blank">تويتر</a></li>
            <li><a href="#" target="_blank">إنستجرام</a></li>
        </ul>
    </div>
    
    <div class="section">
        <ul>
            <li><a href="index.php">الرئيسة</a></li>
        </ul>
    </div>
</nav>

<div class="container">
    <aside class="sidebar" id="sidebar">
        <h3>لوحة التحكم</h3>
        <ul>
            <li><a href="#">الصفحة الرئيسية</a></li>
            <li><a href="#">المنتجات</a></li>
            <li><a href="#">الطلبات</a></li>
            <li><a href="#">الإعدادات</a></li>
            <li><a href="#">معلومات الاتصال</a></li>
            <li><a href="#">تسجيل الخروج</a></li>
        </ul>
    </aside>

    <main>
        <div class="last-post">
            <h4>آخر المشاركات</h4>
            <ul>
                <li><a href="#">
                    <span class="span-img">
                        <img src="placeholder.jpg" alt="Post Image" loading="lazy">
                    </span>
                </a></li>
            </ul>
        </div>

        <div class="cart">
            <ul>
                <li><a href="signup.php"><i class="fas fa-user"></i> تسجيل الدخول</a></li>
                <li class="cart-icon">
                    <a href="cart.php" aria-label="عربة التسوق"><i class="fas fa-shopping-cart"></i></a>
                    <span class="cart-count">0</span>
                </li>
            </ul>
        </div>

        <div class="product">
            <div class="product_img">
                <img src="placeholder.jpg" alt="Product Image" loading="lazy"><span class="unavailable"></span>
            </div>
            <div class="product_name">اسم المنتج</div>
            <div class="product_price">100 ر.س</div>
            <div class="qty_input">
                <button class="qty_count_mins" onclick="updateQuantity(-1)">-</button>
                <input type="number" id="quantity" name="quantity" value="1" min="1" max="100">
                <button class="qty_count_add" onclick="updateQuantity(1)">+</button>
            </div>
            <div class="submit">
                <button class="addto_cart" type="button">
                    <i class="fas fa-cart-plus"></i> إضافة إلى السلة
                </button>
            </div>
        </div>
    </main>
</div>

<div class="settings-panel" id="settings-panel">
    <h3>إعدادات</h3>
    <label>
        <input type="radio" name="theme" value="light" checked onchange="changeTheme()"> الوضع الفاتح
    </label>
    <label>
        <input type="radio" name="theme" value="dark" onchange="changeTheme()"> الوضع الداكن
    </label>
    <button onclick="toggleSettings()">إغلاق</button>
</div>

<footer>
    <p>حقوق النشر &copy; 2024 - جميع الحقوق محفوظة</p>
</footer>

<script src="script.js"></script>
</body>
</html>
