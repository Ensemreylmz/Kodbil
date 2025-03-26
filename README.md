<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <title>KODBİL - Yazılım Öğrenme ve Yarışma Platformu</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* KÖK Değişkenler */
        :root {
            --primary-color: #3f51b5;
            --secondary-color: #ff5722;
            --accent-color: #2196f3;
            --text-color: #333;
            --light-text: #000000;
            --bg-color: #f8f9fa;
            --card-bg: #fff;
            --border-radius: 10px;
            --box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }

        /* ANA İçerik */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
        }

        /* Başlık Stilleri  */
        header {
            padding: 15px 30px;
            background-color: var(--card-bg);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1400px;
            margin: 0 auto;
            width: 100%;
        }

        .logo-container {
            display: flex;
            align-items: center;
            text-decoration: none;
            color: var(--primary-color);
        }

        .logo-icon {
            font-size: 24px;
            margin-right: 10px;
            color: var(--secondary-color);
        }

        .logo-text {
            font-size: 24px;
            font-weight: 700;
            letter-spacing: 1px;
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .nav-link {
            text-decoration: none;
            color: var(--light-text);
            font-weight: 500;
            padding: 8px 12px;
            border-radius: 5px;
            transition: var(--transition);
        }

        .nav-link:hover {
            color: var(--primary-color);
            background-color: rgba(63, 81, 181, 0.05);
        }

        .nav-buttons {
            display: flex;
            gap: 15px;
        }

        .btn {
            padding: 10px 20px;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            text-decoration: none;
            text-align: center;
        }

        .btn-outline {
            border: 2px solid var(--primary-color);
            color: var(--primary-color);
            background-color: transparent;
        }

        .btn-outline:hover {
            background-color: rgba(63, 81, 181, 0.05);
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: white;
            border: 2px solid var(--primary-color);
        }

        .btn-primary:hover {
            background-color: #303f9f;
            border-color: #303f9f;
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 24px;
            color: var(--primary-color);
            cursor: pointer;
        }

        /* Karşılama Bölümü */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 80px 20px;
            color: white;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero-title {
            font-size: 48px;
            font-weight: 800;
            margin-bottom: 20px;
            letter-spacing: 1px;
        }

        .hero-subtitle {
            font-size: 24px;
            font-weight: 300;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
        }

        .btn-hero {
            padding: 14px 30px;
            font-size: 18px;
            border-radius: 30px;
        }

        .btn-light {
            background-color: white;
            color: var(--primary-color);
            border: 2px solid white;
        }

        .btn-light:hover {
            background-color: rgba(255, 255, 255, 0.9);
        }

        .btn-outline-light {
            border: 2px solid white;
            color: white;
            background-color: transparent;
        }

        .btn-outline-light:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }

        /* ANA İçerik */
        main {
            flex: 1;
            padding: 60px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .section-subtitle {
            text-align: center;
            font-size: 18px;
            color: var(--light-text);
            margin-bottom: 60px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        /*  Hakkında Bölümü */
        .about-section {
            margin-bottom: 80px;
        }

        .content-card {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            padding: 40px;
            margin-bottom: 40px;
        }

        .content-card p {
            font-size: 18px;
            color: var(--light-text);
            margin-bottom: 20px;
            line-height: 1.7;
        }

        /* Özellikler Bölümü */
        .features-section {
            margin-bottom: 80px;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .feature-card {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            padding: 30px;
            text-align: center;
            transition: var(--transition);
        }

        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.1);
        }

        .feature-icon {
            font-size: 40px;
            color: var(--secondary-color);
            margin-bottom: 20px;
        }

        .feature-title {
            font-size: 22px;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .feature-description {
            color: var(--light-text);
            line-height: 1.6;
        }

        /* Katagoriler Bölümü */
        .categories-section {
            margin-bottom: 80px;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .category-card {
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            overflow: hidden;
            transition: var(--transition);
        }

        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 25px rgba(0, 0, 0, 0.1);
        }

        .category-header {
            height: 140px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 28px;
            font-weight: 600;
        }

        .category-beginner {
            background: linear-gradient(135deg, #43cea2 0%, #185a9d 100%);
        }

        .category-intermediate {
            background: linear-gradient(135deg, #ff9966 0%, #ff5e62 100%);
        }

        .category-advanced {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
        }

        .category-body {
            padding: 30px;
        }

        .category-title {
            font-size: 22px;
            font-weight: 600;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .category-description {
            color: var(--light-text);
            margin-bottom: 20px;
            line-height: 1.6;
        }

        .category-stats {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
        }

        .stat {
            text-align: center;
        }

        .stat-value {
            font-size: 24px;
            font-weight: 700;
            color: var(--secondary-color);
        }

        .stat-label {
            font-size: 14px;
            color: var(--light-text);
        }

        /* Kayıt Bölümü */
        .cta-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            padding: 80px 20px;
            text-align: center;
            border-radius: var(--border-radius);
            color: white;
            margin-bottom: 80px;
        }

        .cta-title {
            font-size: 36px;
            font-weight: 700;
            margin-bottom: 20px;
        }

        .cta-subtitle {
            font-size: 18px;
            max-width: 600px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }

        /* Login Styles */
        .login-main {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 60px 20px;
        }

        .login-container {
            max-width: 450px;
            width: 100%;
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            padding: 40px;
        }

        .login-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .login-title {
            font-size: 28px;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        .login-subtitle {
            color: var(--light-text);
            font-size: 16px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-label {
            display: block;
            font-weight: 600;
            margin-bottom: 8px;
            color: var(--text-color);
        }

        .form-input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 6px;
            font-size: 16px;
            transition: var(--transition);
        }

        .form-input:focus {
            border-color: var(--primary-color);
            outline: none;
            box-shadow: 0 0 0 2px rgba(63, 81, 181, 0.2);
        }

        .form-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
        }

        .form-checkbox-label {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
        }

        .form-checkbox {
            width: 16px;
            height: 16px;
            cursor: pointer;
        }

        .forgot-password {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            transition: var(--transition);
        }

        .forgot-password:hover {
            text-decoration: underline;
        }

        .login-btn {
            width: 100%;
            padding: 14px;
            font-size: 16px;
            margin-bottom: 20px;
        }

        .login-divider {
            display: flex;
            align-items: center;
            margin: 20px 0;
        }

        .login-divider::before,
        .login-divider::after {
            content: "";
            flex: 1;
            height: 1px;
            background-color: #ddd;
        }

        .login-divider-text {
            padding: 0 15px;
            color: #777;
        }

        .social-login {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }

        .social-btn {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 10px;
            padding: 12px;
            border-radius: 6px;
            border: 1px solid #ddd;
            background-color: white;
            text-decoration: none;
            color: var(--text-color);
            transition: var(--transition);
        }

        .social-btn:hover {
            background-color: #f5f5f5;
        }

        .register-link {
            text-align: center;
            font-size: 15px;
        }

        .register-link a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
        }

        .register-link a:hover {
            text-decoration: underline;
        }

        /* Kayıt Sayfası Stilleri */
        .register-main {
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 60px 20px;
        }

        .register-container {
            max-width: 500px;
            width: 100%;
            background-color: var(--card-bg);
            border-radius: var(--border-radius);
            box-shadow: var(--box-shadow);
            padding: 40px;
        }

        .register-header {
            text-align: center;
            margin-bottom: 30px;
        }

        .register-title {
            font-size: 28px;
            font-weight: 700;
            color: var(--primary-color);
            margin-bottom: 10px;
        }

        .register-subtitle {
            color: var(--light-text);
            font-size: 16px;
        }

        .form-row {
            display: flex;
            gap: 15px;
        }

        .form-row .form-group {
            flex: 1;
        }

        .form-terms {
            margin-bottom: 25px;
        }

        .form-checkbox-label {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            cursor: pointer;
        }

        .form-checkbox {
            width: 16px;
            height: 16px;
            margin-top: 3px;
            cursor: pointer;
        }

        .terms-link {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
        }

        .terms-link:hover {
            text-decoration: underline;
        }

        .register-btn {
            width: 100%;
            padding: 14px;
            font-size: 16px;
            margin-bottom: 20px;
        }

        .login-link {
            text-align: center;
            font-size: 15px;
        }

        .login-link a {
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 600;
        }

        .login-link a:hover {
            text-decoration: underline;
        }

        .register-divider {
            display: flex;
            align-items: center;
            margin: 20px 0;
        }

        .register-divider::before,
        .register-divider::after {
            content: "";
            flex: 1;
            height: 1px;
            background-color: #ddd;
        }

        .register-divider-text {
            padding: 0 15px;
            color: #777;
        }

        .social-register {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }

        /* Genel stil eklentileri */
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <a href="#" class="logo-container">
                <i class="fas fa-code logo-icon"></i>
                <span class="logo-text">KODBİL</span>
            </a>

            <div class="nav-links">
                <a href="#about" class="nav-link">Hakkımızda</a>
                <a href="#features" class="nav-link">Özellikler</a>
                <a href="#categories" class="nav-link">Kategoriler</a>
            </div>

            <div class="nav-buttons">
                <a href="#" class="btn btn-outline" id="leaderboardBtn">Sıralama Tablosu</a>
                <a href="#" class="btn btn-outline" id="registerHeaderBtn">Kayıt Ol</a>
                <a href="#" class="btn btn-primary" id="loginBtn">Giriş Yap</a>
            </div>

            <button class="mobile-menu-btn">
                <i class="fas fa-bars"></i>
            </button>
        </nav>
    </header>

    <!-- Ana Sayfa İçeriği -->
    <div id="homePage">
        <section class="hero">
            <div class="hero-content">
                <h1 class="hero-title">Kodlama Becerilerini Geliştir ve Yarış</h1>
                <p class="hero-subtitle">KODBİL ile yazılım dünyasındaki yetkinliklerini test et, yeni beceriler kazan ve diğer geliştiricilerle rekabet et.</p>
                <div class="hero-buttons">
                    <a href="#" class="btn btn-hero btn-light" id="startNowBtn">Hemen Başla</a>
                    <a href="#about" class="btn btn-hero btn-outline-light">Daha Fazla Bilgi</a>
                </div>
            </div>
        </section>

        <main>
            <div class="container">
                <section id="about" class="about-section">
                    <h2 class="section-title">KODBİL Nedir?</h2>
                    <p class="section-subtitle">Yazılım dünyasında kendinizi geliştirmenin en etkili yolu</p>

                    <div class="content-card">
                        <p>KodBil, yazılım öğrenmek veya mevcut yeteneklerini geliştirmek isteyen herkes için tasarlanmış bir platformdur. Web tabanlı olarak geliştirilecek olan bu yarışma, yazılım dilleri, algoritmalar, veri yapıları, bilişim ve yazılım mühendisliği gibi alanlarda geniş bir soru havuzuna sahip olacak. Sorular, kolay, orta ve zor şeklinde kategorilere ayrılacak, böylece her seviyeden katılımcı kendi becerilerini test edebilecek.</p>
                        
                        <p>Platform, kullanıcıların programlama becerilerini geliştirirken aynı zamanda rekabetçi bir ortamda kendilerini test etmelerine olanak tanır. Düzenli olarak güncellenen soru havuzu ve gerçek hayat problemlerine dayalı zorluklarla, KODBİL sadece teorik bilgiyi değil, pratik uygulama kabiliyetini de ölçer.</p>
                    </div>
                </section>

                <section id="features" class="features-section">
                    <h2 class="section-title">Özellikler</h2>
                    <p class="section-subtitle">KODBİL'in sunduğu avantajlar</p>

                    <div class="features-grid">
                        <div class="feature-card">
                            <i class="fas fa-laptop-code feature-icon"></i>
                            <h3 class="feature-title">Geniş Soru Havuzu</h3>
                            <p class="feature-description">Farklı zorluk seviyelerinde ve konularda binlerce soru ile becerilerinizi geliştirebilirsiniz.</p>
                        </div>

                        <div class="feature-card">
                            <i class="fas fa-trophy feature-icon"></i>
                            <h3 class="feature-title">Rekabetçi Sıralama</h3>
                            <p class="feature-description">Diğer kullanıcılarla yarışarak motivasyonunuzu yüksek tutun ve liderlik tablosunda yerinizi alın.</p>
                        </div>

                        <div class="feature-card">
                            <i class="fas fa-chart-line feature-icon"></i>
                            <h3 class="feature-title">İlerleme Takibi</h3>
                            <p class="feature-description">Detaylı istatistikler ve grafikler ile kendi gelişiminizi izleyin ve zayıf yönlerinizi belirleyin.</p>
                        </div>
                    </div>
                </section>

                <section id="categories" class="categories-section">
                    <h2 class="section-title">Zorluk Kategorileri</h2>
                    <p class="section-subtitle">Her seviyeye uygun içerikler ile programlama yolculuğunuzda ilerleyin</p>

                    <div class="categories-grid">
                        <div class="category-card">
                            <div class="category-header category-beginner">
                                <h3>Kolay</h3>
                            </div>
                            <div class="category-body">
                                <h4 class="category-title">Yeni Başlayanlar İçin</h4>
                                <p class="category-description">Temel kavramları öğrenmek ve programlamaya adım atmak isteyenler için ideal. Basit algoritma problemleri, veri yapıları ve dil özellikleri.</p>
                                <div class="category-stats">
                                    <div class="stat">
                                        <div class="stat-value">500+</div>
                                        <div class="stat-label">Soru</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">10K+</div>
                                        <div class="stat-label">Çözüm</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">15+</div>
                                        <div class="stat-label">Konu</div>
                                    </div>
                                </div>
                                <a href="#" class="btn btn-outline">Başla</a>
                            </div>
                        </div>

                        <div class="category-card">
                            <div class="category-header category-intermediate">
                                <h3>Orta</h3>
                            </div>
                            <div class="category-body">
                                <h4 class="category-title">Deneyim Kazananlar İçin</h4>
                                <p class="category-description">Temel bilgisini geliştirmek ve daha karmaşık problemleri çözmek isteyenler için. Algoritma optimizasyonu, orta düzey veri yapıları ve gerçek dünya uygulamaları.</p>
                                <div class="category-stats">
                                    <div class="stat">
                                        <div class="stat-value">750+</div>
                                        <div class="stat-label">Soru</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">8K+</div>
                                        <div class="stat-label">Çözüm</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">20+</div>
                                        <div class="stat-label">Konu</div>
                                    </div>
                                </div>
                                <a href="#" class="btn btn-outline">Başla</a>
                            </div>
                        </div>

                        <div class="category-card">
                            <div class="category-header category-advanced">
                                <h3>Zor</h3>
                            </div>
                            <div class="category-body">
                                <h4 class="category-title">Uzmanlar İçin</h4>
                                <p class="category-description">İleri düzey programcılar ve yazılım mühendisleri için zorlayıcı problemler. Karmaşık algoritmalar, optimizasyon teknikleri ve üst düzey sistem tasarımı konuları.</p>
                                <div class="category-stats">
                                    <div class="stat">
                                        <div class="stat-value">300+</div>
                                        <div class="stat-label">Soru</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">3K+</div>
                                        <div class="stat-label">Çözüm</div>
                                    </div>
                                    <div class="stat">
                                        <div class="stat-value">25+</div>
                                        <div class="stat-label">Konu</div>
                                    </div>
                                </div>
                                <a href="#" class="btn btn-outline">Başla</a>
                            </div>
                        </div>
                    </div>
                </section>

                <section class="cta-section">
                    <h2 class="cta-title">Programlama Yolculuğunuza Bugün Başlayın</h2>
                    <p class="cta-subtitle">Hemen kaydolun ve kodlama becerilerinizi geliştirmeye başlayın. İlk ay tamamen ücretsiz!</p>
                    <a href="#" class="btn btn-hero btn-light" id="registerCTA">Ücretsiz Kaydol</a>
                </section>
            </div>
        </main>
    </div>
    

    <!-- Giriş Sayfası İçeriği -->
    <div id="loginPage" class="hidden">
        <main class="login-main">
            <div class="login-container">
                <div class="login-header">
                    <h1 class="login-title">Giriş Yap</h1>
                    <p class="login-subtitle">KODBİL hesabınıza erişin</p>
                </div>

                <form action="#" method="post">
                    <div class="form-group">
                        <label for="email" class="form-label">E-posta Adresi</label>
                        <input type="email" id="email" name="email" class="form-input" placeholder="E-posta adresiniz" required>
                    </div>

                    <div class="form-group">
                        <label for="password" class="form-label">Şifre</label>
                        <input type="password" id="password" name="password" class="form-input" placeholder="Şifreniz" required>
                    </div>

                    <div class="form-footer">
                        <label class="form-checkbox-label">
                            <input type="checkbox" class="form-checkbox" name="remember">
                            Beni hatırla
                        </label>
                        <a href="#" class="forgot-password">Şifremi unuttum</a>
                    </div>

                    <button type="submit" class="btn btn-primary login-btn">Giriş Yap</button>
                </form>

                <div class="login-divider">
                    <span class="login-divider-text">veya</span>
                </div>

                <div class="social-login">
                    <a href="#" class="social-btn">
                        <i class="fab fa-google"></i>
                        Google
                    </a>
                </div>

                <div class="register-link">
                    Hesabınız yok mu? <a href="#" id="registerBtn">Hesabınız yok mu? <a href="#" id="registerBtn">Hesap Oluştur</a>
                </div>
            </div>
        </main>
    </div>

    <!-- Kayıt Sayfası İçeriği -->
    <div id="registerPage" class="hidden">
        <main class="register-main">
            <div class="register-container">
                <div class="register-header">
                    <h1 class="register-title">Hesap Oluştur</h1>
                    <p class="register-subtitle">KODBİL'e üye olarak kodlama yolculuğunuza başlayın</p>
                </div>

                <form action="#" method="post">
                    <div class="form-row">
                        <div class="form-group">
                            <label for="firstName" class="form-label">Ad</label>
                            <input type="text" id="firstName" name="firstName" class="form-input" placeholder="Adınız" required>
                        </div>
                        <div class="form-group">
                            <label for="lastName" class="form-label">Soyad</label>
                            <input type="text" id="lastName" name="lastName" class="form-input" placeholder="Soyadınız" required>
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="regEmail" class="form-label">E-posta Adresi</label>
                        <input type="email" id="regEmail" name="email" class="form-input" placeholder="E-posta adresiniz" required>
                    </div>

                    <div class="form-group">
                        <label for="regPassword" class="form-label">Şifre</label>
                        <input type="password" id="regPassword" name="password" class="form-input" placeholder="En az 8 karakter" required>
                    </div>

                    <div class="form-group">
                        <label for="confirmPassword" class="form-label">Şifre Tekrar</label>
                        <input type="password" id="confirmPassword" name="confirmPassword" class="form-input" placeholder="Şifrenizi tekrar girin" required>
                    </div>

                    <div class="form-terms">
                        <label class="form-checkbox-label">
                            <input type="checkbox" class="form-checkbox" name="terms" required>
                            <span>
                                <a href="#" class="terms-link">Kullanım Şartları</a> ve <a href="#" class="terms-link">Gizlilik Politikası</a>'nı okudum ve kabul ediyorum.
                            </span>
                        </label>
                    </div>

                    <button type="submit" class="btn btn-primary register-btn">Kayıt Ol</button>
                </form>

                <div class="register-divider">
                    <span class="register-divider-text">veya</span>
                </div>

                <div class="social-register">
                    <a href="#" class="social-btn">
                        <i class="fab fa-google"></i>
                        Google ile Kaydol
                    </a>
                </div>

                <div class="login-link">
                    Zaten bir hesabınız var mı? <a href="#" id="loginLinkBtn">Giriş Yap</a>
            
    </footer>

    <script>

        // KODBİL yazısına veya logoya tıklayınca ana sayfaya dönüş
         document.querySelector('.logo-container').addEventListener('click', function(e) {e.preventDefault();
         homePage.classList.remove('hidden');
         loginPage.classList.add('hidden');
         registerPage.classList.add('hidden');
});
        // Sayfa geçişleri için basit JavaScript
        document.addEventListener('DOMContentLoaded', function() {
            const homePage = document.getElementById('homePage');
            const loginPage = document.getElementById('loginPage');
            const registerPage = document.getElementById('registerPage');

            // Ana sayfadan kayıt sayfasına geçiş (başlık butonu)
        document.getElementById('registerHeaderBtn').addEventListener('click', function(e) {e.preventDefault();
            homePage.classList.add('hidden');
            loginPage.classList.add('hidden');
            registerPage.classList.remove('hidden');});
            
            // Ana sayfadan giriş sayfasına geçiş
            document.getElementById('loginBtn').addEventListener('click', function(e) {
                e.preventDefault();
                homePage.classList.add('hidden');
                registerPage.classList.add('hidden');
                loginPage.classList.remove('hidden');
            });
            
            // Ana sayfadan kayıt sayfasına geçiş
            document.getElementById('startNowBtn').addEventListener('click', function(e) {
                e.preventDefault();
                homePage.classList.add('hidden');
                loginPage.classList.add('hidden');
                registerPage.classList.remove('hidden');
            });
            
            // CTA butonundan kayıt sayfasına geçiş
            document.getElementById('registerCTA').addEventListener('click', function(e) {
                e.preventDefault();
                homePage.classList.add('hidden');
                loginPage.classList.add('hidden');
                registerPage.classList.remove('hidden');
            });
            
            // Giriş sayfasından kayıt sayfasına geçiş
            document.getElementById('registerBtn').addEventListener('click', function(e) {
                e.preventDefault();
                loginPage.classList.add('hidden');
                registerPage.classList.remove('hidden');
            });
            
            
            // Kayıt sayfasından giriş sayfasına geçiş
            document.getElementById('loginLinkBtn').addEventListener('click', function(e) {
                e.preventDefault();
                registerPage.classList.add('hidden');
                loginPage.classList.remove('hidden');
            });

            // Footer stilleri için CSS eklemeleri
            const style = document.createElement('style');
            style.textContent = `
                footer {
                    background-color: var(--primary-color);
                    color: white;
                    padding: 60px 0 20px;
                }
                
                .footer-content {
                    display: flex;
                    flex-wrap: wrap;
                    justify-content: space-between;
                    margin-bottom: 40px;
                }
                
                .footer-logo {
                    display: flex;
                    align-items: center;
                    margin-bottom: 20px;
                }
                
                .footer-logo .logo-icon {
                    font-size: 24px;
                    margin-right: 10px;
                    color: var(--secondary-color);
                }
                
                .footer-logo .logo-text {
                    font-size: 24px;
                    font-weight: 700;
                    letter-spacing: 1px;
                }
                
                .footer-links {
                    display: flex;
                    flex-wrap: wrap;
                    gap: 60px;
                }
                
                .footer-section h4 {
                    font-size: 18px;
                    margin-bottom: 20px;
                    font-weight: 600;
                }
                
                .footer-section ul {
                    list-style: none;
                    padding: 0;
                }
                
                .footer-section ul li {
                    margin-bottom: 10px;
                }
                
                .footer-section ul li a {
                    color: rgba(255, 255, 255, 0.8);
                    text-decoration: none;
                    transition: var(--transition);
                }
                
                .footer-section ul li a:hover {
                    color: white;
                }
                
                .footer-bottom {
                    display: flex;
                    justify-content: space-between;
                    align-items: center;
                    padding-top: 20px;
                    border-top: 1px solid rgba(255, 255, 255, 0.1);
                }
                
                .social-links {
                    display: flex;
                    gap: 15px;
                }
                
                .social-links a {
                    color: white;
                    font-size: 18px;
                    transition: var(--transition);
                }
                
                .social-links a:hover {
                    color: var(--secondary-color);
                }
                
                @media (max-width: 768px) {
                    .footer-content {
                        flex-direction: column;
                    }
                    
                    .footer-links {
                        flex-direction: column;
                        gap: 30px;
                    }
                    
                    .footer-bottom {
                        flex-direction: column;
                        gap: 20px;
                        text-align: center;
                    }
                    
                    .nav-links, .nav-buttons {
                        display: none;
                    }
                    
                    .mobile-menu-btn {
                        display: block;
                    }
                    
                    .hero-title {
                        font-size: 36px;
                    }
                    
                    .hero-subtitle {
                        font-size: 18px;
                    }
                    
                    .hero-buttons {
                        flex-direction: column;
                        gap: 15px;
                    }
                }
            `;
            document.head.appendChild(style);
        });
        
    </script>
</body>
</html>
