# Unison-AI-Platform
UNISON is a holistic aid platform that empowers disaster responders by providing critical real-time information and tools for resource coordination. It uniquely integrates spiritual and emotional care to support responder resilience and well-being throughout their mission.
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Unison AI - 公益救援领袖的智能心灵伙伴</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* 全局样式 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --primary: #4A7C59;
            --primary-light: #8FB996;
            --primary-dark: #3A5F4B;
            --secondary: #C8D5B9;
            --accent: #68A691;
            --wood: #D4A574;
            --wood-light: #FAEDCA;
            --wood-dark: #8B7355;
            --dark: #3A4A3F;
            --light: #F9F7F3;
            --gray: #95A5A6;
            --gray-light: #ECF0F1;
            --danger: #E74C3C;
            --warning: #F39C12;
            --info: #3498DB;
            --success: #27AE60;
        }
        
        body {
            font-family: "Microsoft YaHei", "微软雅黑", "Segoe UI", sans-serif;
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            min-height: 100vh;
            overflow-x: hidden;
            letter-spacing: 0.3px;
            background-image: 
                radial-gradient(circle at 10% 20%, rgba(143, 185, 150, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 90% 80%, rgba(212, 165, 116, 0.05) 0%, transparent 20%);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* 头部区域 */
        .site-header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
            border-bottom: 1px solid rgba(74, 124, 89, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }
        
        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo-icon {
            font-size: 2.5rem;
            color: var(--primary);
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .logo-text {
            display: flex;
            flex-direction: column;
            line-height: 1.2;
        }
        
        .logo-main {
            font-size: 2rem;
            font-weight: 700;
            color: var(--primary);
            letter-spacing: 1px;
        }
        
        .logo-sub {
            font-size: 0.9rem;
            color: var(--wood-dark);
            font-weight: 300;
            letter-spacing: 1px;
        }
        
        .slogan {
            font-size: 1.2rem;
            font-weight: 400;
            color: var(--dark);
            font-style: italic;
            margin-left: 20px;
            padding-left: 20px;
            border-left: 2px solid var(--primary-light);
        }
        
        .nav-buttons {
            display: flex;
            gap: 15px;
        }
        
        .btn {
            padding: 10px 24px;
            border-radius: 50px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: 2px solid var(--primary);
            font-size: 1rem;
        }
        
        .btn-outline {
            background: transparent;
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background: var(--primary);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(74, 124, 89, 0.2);
        }
        
        .btn-primary {
            background: var(--primary);
            color: white;
        }
        
        .btn-primary:hover {
            background: var(--primary-dark);
            transform: translateY(-2px);
            box-shadow: 0 8px 15px rgba(74, 124, 89, 0.2);
        }
        
        /* 英雄区域 */
        .hero {
            padding: 80px 0 60px;
            text-align: center;
        }
        
        .hero-title {
            font-size: 3rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: var(--dark);
        }
        
        .hero-highlight {
            color: var(--primary);
            position: relative;
            display: inline-block;
        }
        
        .hero-highlight::after {
            content: "";
            position: absolute;
            bottom: 5px;
            left: 0;
            width: 100%;
            height: 8px;
            background-color: rgba(143, 185, 150, 0.3);
            z-index: -1;
            border-radius: 4px;
        }
        
        .hero-description {
            font-size: 1.3rem;
            color: var(--dark);
            margin-bottom: 2.5rem;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            opacity: 0.9;
            font-weight: 300;
            line-height: 1.8;
        }
        
        .hero-cta {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 2rem;
        }
        
        /* 核心功能 */
        .section-title {
            font-size: 2.2rem;
            font-weight: 600;
            text-align: center;
            margin-bottom: 3rem;
            color: var(--dark);
            position: relative;
            padding-bottom: 15px;
        }
        
        .section-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary) 0%, var(--accent) 100%);
            border-radius: 2px;
        }
        
        .features {
            padding: 80px 0;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }
        
        .feature-card {
            background: white;
            border-radius: 16px;
            padding: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.1);
            position: relative;
            overflow: hidden;
            height: 100%;
            display: flex;
            flex-direction: column;
            border: 1px solid rgba(74, 124, 89, 0.1);
            background: linear-gradient(to bottom, white 0%, #f9f9f9 100%);
        }
        
        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            border-color: var(--primary-light);
        }
        
        .feature-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary) 0%, var(--accent) 100%);
        }
        
        .feature-number {
            position: absolute;
            top: 15px;
            right: 20px;
            font-size: 3rem;
            font-weight: 700;
            color: rgba(74, 124, 89, 0.08);
            line-height: 1;
        }
        
        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .feature-title {
            font-size: 1.5rem;
            font-weight: 600;
            margin-bottom: 1rem;
            color: var(--dark);
        }
        
        .feature-description {
            color: var(--dark);
            margin-bottom: 1.5rem;
            flex-grow: 1;
            opacity: 0.8;
            font-weight: 300;
            line-height: 1.7;
        }
        
        .feature-example {
            background: linear-gradient(135deg, rgba(74, 124, 89, 0.05) 0%, rgba(143, 185, 150, 0.05) 100%);
            border-left: 4px solid var(--primary);
            padding: 1.2rem;
            border-radius: 0 8px 8px 0;
            margin-top: 1rem;
            font-style: italic;
            color: var(--primary);
            font-weight: 300;
            border: 1px solid rgba(74, 124, 89, 0.1);
            border-left-width: 4px;
        }
        
        /* 宁静守护模式 */
        .serenity-section {
            padding: 80px 0;
            background: linear-gradient(135deg, rgba(74, 124, 89, 0.03) 0%, rgba(143, 185, 150, 0.03) 100%);
            border-top: 1px solid rgba(74, 124, 89, 0.05);
            border-bottom: 1px solid rgba(74, 124, 89, 0.05);
        }
        
        .serenity-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }
        
        .serenity-description {
            font-size: 1.2rem;
            color: var(--dark);
            margin-bottom: 2.5rem;
            opacity: 0.9;
            font-weight: 300;
            line-height: 1.8;
        }
        
        .serenity-demo {
            background: 
                linear-gradient(135deg, rgba(58, 74, 63, 0.95) 0%, rgba(74, 124, 89, 0.95) 100%),
                url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><path d="M0,0 L100,0 L100,100 Z" fill="%234A7C59" opacity="0.05"/></svg>');
            border-radius: 20px;
            padding: 3.5rem;
            color: white;
            text-align: center;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(74, 124, 89, 0.3);
            margin-top: 2rem;
        }
        
        .serenity-demo::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none" opacity="0.05"><path d="M0,0 L100,0 L100,100 Z" fill="white"/></svg>');
            background-size: cover;
        }
        
        .serenity-title {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: white;
            position: relative;
            font-weight: 600;
        }
        
        .serenity-quote {
            font-size: 1.3rem;
            font-style: italic;
            margin-bottom: 2rem;
            color: rgba(255, 255, 255, 0.9);
            line-height: 1.8;
            position: relative;
            font-weight: 300;
        }
        
        .serenity-btn {
            background: transparent;
            border: 2px solid rgba(255, 255, 255, 0.3);
            color: white;
            padding: 16px 40px;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            margin-top: 1rem;
            position: relative;
        }
        
        .serenity-btn:hover {
            background: rgba(255, 255, 255, 0.1);
            border-color: white;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        /* 注册区域 */
        .register-section {
            padding: 80px 0;
        }
        
        .register-card {
            background: white;
            border-radius: 20px;
            padding: 3rem;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
            border: 1px solid rgba(74, 124, 89, 0.1);
            background: linear-gradient(to bottom, white 0%, #f9f9f9 100%);
            position: relative;
            overflow: hidden;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .register-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, var(--primary) 0%, var(--accent) 100%);
        }
        
        .register-title {
            font-size: 2rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            text-align: center;
            color: var(--dark);
        }
        
        .register-subtitle {
            text-align: center;
            color: var(--gray);
            margin-bottom: 2rem;
            font-weight: 300;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--dark);
        }
        
        .form-input {
            width: 100%;
            padding: 15px 20px;
            border: 2px solid var(--gray-light);
            border-radius: 10px;
            font-size: 1rem;
            transition: all 0.3s ease;
            background-color: white;
        }
        
        .form-input:focus {
            border-color: var(--primary);
            outline: none;
            box-shadow: 0 0 0 3px rgba(74, 124, 89, 0.1);
        }
        
        .role-selector {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-top: 10px;
        }
        
        .role-option {
            border: 2px solid var(--gray-light);
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 300;
            background-color: white;
        }
        
        .role-option:hover {
            border-color: var(--primary-light);
            background-color: rgba(74, 124, 89, 0.05);
        }
        
        .role-option.selected {
            border-color: var(--primary);
            background-color: rgba(74, 124, 89, 0.1);
            font-weight: 500;
        }
        
        .role-icon {
            font-size: 1.8rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .form-footer {
            text-align: center;
            margin-top: 30px;
        }
        
        .btn-register {
            background: linear-gradient(135deg, var(--primary) 0%, var(--accent) 100%);
            color: white;
            width: 100%;
            padding: 16px;
            font-size: 1.1rem;
            margin-bottom: 20px;
            border: none;
            border-radius: 10px;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        .btn-register:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(74, 124, 89, 0.3);
        }
        
        .login-link {
            color: var(--primary);
            text-decoration: none;
            font-weight: 500;
        }
        
        .login-link:hover {
            text-decoration: underline;
        }
        
        /* 页脚 */
        footer {
            background: 
                linear-gradient(135deg, var(--dark) 0%, #2a3a2f 100%),
                url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><path d="M0,0 L100,0 L100,100 Z" fill="%234A7C59" opacity="0.05"/></svg>');
            color: white;
            padding: 60px 0 30px;
            border-top: 5px solid var(--primary);
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: white;
            font-weight: 600;
            position: relative;
            padding-bottom: 10px;
        }
        
        .footer-section h3::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 40px;
            height: 3px;
            background-color: var(--primary-light);
            border-radius: 3px;
        }
        
        .footer-section p, .footer-section a {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: color 0.3s ease;
            font-weight: 300;
            line-height: 1.7;
        }
        
        .footer-section a:hover {
            color: white;
            padding-left: 5px;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
            font-weight: 300;
        }
        
        /* 响应式设计 */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                gap: 20px;
            }
            
            .slogan {
                margin-left: 0;
                padding-left: 0;
                border-left: none;
                border-top: 2px solid var(--primary-light);
                padding-top: 10px;
                text-align: center;
                margin-top: 10px;
            }
            
            .logo-container {
                flex-direction: column;
                text-align: center;
            }
            
            .hero-title {
                font-size: 2.2rem;
            }
            
            .hero-cta {
                flex-direction: column;
                align-items: center;
            }
            
            .features-grid {
                grid-template-columns: 1fr;
            }
            
            .role-selector {
                grid-template-columns: 1fr;
            }
            
            .serenity-demo {
                padding: 2.5rem 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- 头部 -->
    <header class="site-header">
        <div class="container">
            <div class="header-content">
                <div class="logo-container">
                    <div class="logo-icon">
                        <i class="fas fa-hands-helping"></i>
                    </div>
                    <div class="logo-text">
                        <div class="logo-main">Unison AI</div>
                        <div class="logo-sub">智能心灵伙伴</div>
                    </div>
                    <div class="slogan">你照顾世界，我们照顾你</div>
                </div>
                
                <div class="nav-buttons">
                    <button class="btn btn-outline" id="loginBtn">
                        <i class="fas fa-sign-in-alt"></i> 登录
                    </button>
                    <button class="btn btn-primary" id="registerBtn">
                        <i class="fas fa-user-plus"></i> 立即体验
                    </button>
                </div>
            </div>
        </div>
    </header>
    
    <!-- 主要内容 -->
    <main>
        <!-- 英雄区域 -->
        <section class="hero">
            <div class="container">
                <h1 class="hero-title">Unison AI：公益救援领袖的<span class="hero-highlight">智能心灵伙伴</span></h1>
                <p class="hero-description">专为公益救援领袖打造的智能平台，结合AI技术与人性关怀，在高效匹配资源的同时，守护每一位前线领袖的心灵健康。</p>
                <div class="hero-cta">
                    <button class="btn btn-primary" id="heroRegisterBtn" style="padding: 15px 40px; font-size: 1.1rem;">
                        <i class="fas fa-hands-helping"></i> 立即加入互助网络
                    </button>
                    <button class="btn btn-outline" id="learnMoreBtn" style="padding: 15px 40px; font-size: 1.1rem;">
                        <i class="fas fa-play-circle"></i> 观看介绍
                    </button>
                </div>
            </div>
        </section>
        
        <!-- 核心功能 -->
        <section class="features" id="features">
            <div class="container">
                <h2 class="section-title">四大核心功能</h2>
                <div class="features-grid">
                    <div class="feature-card">
                        <div class="feature-number">01</div>
                        <div class="feature-icon">
                            <i class="fas fa-microphone-alt"></i>
                        </div>
                        <h3 class="feature-title">一键清点 & 一句话匹配</h3>
                        <p class="feature-description">通过拍照或语音快速提交需求与捐赠，AI自动识别、整理与匹配，让您从繁琐表格中解放，回归最自然的沟通方式。</p>
                        <div class="feature-example">
                            "我们在XX村，急需500箱水、100顶帐篷..."
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-number">02</div>
                        <div class="feature-icon">
                            <i class="fas fa-broadcast-tower"></i>
                        </div>
                        <h3 class="feature-title">智能前线消息系统</h3>
                        <p class="feature-description">后台智能处理前线消息，定向推送关键信息，避免信息过载，让您专注最重要的事务。</p>
                        <div class="feature-example">
                            "📍王家坝水位上涨至警戒线，急需沙袋支援！"
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-number">03</div>
                        <div class="feature-icon">
                            <i class="fas fa-spa"></i>
                        </div>
                        <h3 class="feature-title">宁静守护模式</h3>
                        <p class="feature-description">当您需要充电时，进入专属的宁静空间。沉浸式音频引导连接自然与内心，获得深层灵性能量补充与恢复。</p>
                        <div class="feature-example">
                            "此刻，你肩上的重担，请暂时交给大地..."
                        </div>
                    </div>
                    
                    <div class="feature-card">
                        <div class="feature-number">04</div>
                        <div class="feature-icon">
                            <i class="fas fa-heart-circle-check"></i>
                        </div>
                        <h3 class="feature-title">灵性共鸣网络</h3>
                        <p class="feature-description">基于信任与关怀的伙伴网络，当系统感知您可能需要支持时，会优雅地通知您的"心灵伙伴"，提供温暖支持与分担。</p>
                        <div class="feature-example">
                            "您的伙伴可能正在深水区航行，一句问候或许是一盏灯..."
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 宁静守护模式 -->
        <section class="serenity-section" id="serenity">
            <div class="container">
                <div class="serenity-content">
                    <h2 class="section-title">宁静守护模式</h2>
                    <p class="serenity-description">这不是一个监测系统，而是一个邀请系统。我们不对领袖进行冷冰冰的数据分析，而是提供一座随时可以进入的"心灵后花园"。</p>
                    
                    <div class="serenity-demo">
                        <h3 class="serenity-title">体验宁静守护</h3>
                        <p class="serenity-quote">"救援工作是一场马拉松，不是短跑。在救助他人的同时，也需要关怀自己。此刻，你肩上的重担，请暂时交给大地。深呼吸，感受身体与地球的连接..."</p>
                        <button class="serenity-btn" id="serenityBtn">
                            <i class="fas fa-play-circle"></i> 体验宁静守护模式
                        </button>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- 注册区域 -->
        <section class="register-section" id="register">
            <div class="container">
                <div class="register-card">
                    <div class="register-header">
                        <h2 class="register-title">加入Unison互助网络</h2>
                        <p class="register-subtitle">成为公益救援领袖社区的一员，体验AI赋能与人性关怀</p>
                    </div>
                    
                    <form id="registerForm">
                        <div class="form-group">
                            <label for="fullName" class="form-label">姓名</label>
                            <input type="text" id="fullName" class="form-input" placeholder="请输入您的真实姓名" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email" class="form-label">电子邮箱</label>
                            <input type="email" id="email" class="form-input" placeholder="example@email.com" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="phone" class="form-label">手机号码</label>
                            <input type="tel" id="phone" class="form-input" placeholder="请输入您的手机号码" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="password" class="form-label">密码</label>
                            <input type="password" id="password" class="form-input" placeholder="至少8位字符，包含字母和数字" required>
                        </div>
                        
                        <div class="form-group">
                            <label class="form-label">您的主要角色</label>
                            <div class="role-selector">
                                <div class="role-option" data-role="rescue_leader">
                                    <div class="role-icon">
                                        <i class="fas fa-user-shield"></i>
                                    </div>
                                    <div>救援队领袖</div>
                                </div>
                                <div class="role-option" data-role="social_worker">
                                    <div class="role-icon">
                                        <i class="fas fa-hands-helping"></i>
                                    </div>
                                    <div>社工/公益领袖</div>
                                </div>
                                <div class="role-option" data-role="donor">
                                    <div class="role-icon">
                                        <i class="fas fa-hand-holding-heart"></i>
                                    </div>
                                    <div>捐赠方代表</div>
                                </div>
                                <div class="role-option" data-role="volunteer">
                                    <div class="role-icon">
                                        <i class="fas fa-users"></i>
                                    </div>
                                    <div>志愿者协调员</div>
                                </div>
                            </div>
                            <input type="hidden" id="role" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="organization" class="form-label">所属组织 (选填)</label>
                            <input type="text" id="organization" class="form-input" placeholder="您所在的公益组织名称">
                        </div>
                        
                        <div class="form-footer">
                            <button type="submit" class="btn-register">
                                <i class="fas fa-hands-helping"></i> 加入Unison互助网络
                            </button>
                            <p>已有账户？ <a href="#" class="login-link" id="toLoginLink">立即登录</a></p>
                        </div>
                    </form>
                </div>
            </div>
        </section>
    </main>
    
    <!-- 页脚 -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section" id="about">
                    <h3>Unison AI平台</h3>
                    <p>你照顾世界，我们照顾你。一个专为公益救援领袖打造的平台，结合AI技术与人性关怀，在高效匹配资源的同时，守护每一位前线领袖的心灵健康。</p>
                    <p><i class="fas fa-map-marker-alt"></i> 台北市公益路一段100号</p>
                </div>
                
                <div class="footer-section">
                    <h3>核心功能</h3>
                    <a href="#features">一键清点 & 匹配</a>
                    <a href="#features">智能前线消息</a>
                    <a href="#serenity">宁静守护模式</a>
                    <a href="#features">灵性共鸣网络</a>
                </div>
                
                <div class="footer-section">
                    <h3>联系我们</h3>
                    <p><i class="fas fa-envelope"></i> contact@unison-ai.org</p>
                    <p><i class="fas fa-phone"></i> (02) 1234-5678</p>
                    <p><i class="fas fa-clock"></i> 周一至周五 9:00-18:00</p>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Unison AI公益救援平台. 本平台致力于服务所有公益救援领袖.</p>
            </div>
        </div>
    </footer>

    <script>
        // 页面元素
        const homeContent = document.getElementById('homeContent');
        const registerBtn = document.getElementById('registerBtn');
        const heroRegisterBtn = document.getElementById('heroRegisterBtn');
        const loginBtn = document.getElementById('loginBtn');
        const learnMoreBtn = document.getElementById('learnMoreBtn');
        const toLoginLink = document.getElementById('toLoginLink');
        const registerForm = document.getElementById('registerForm');
        const roleOptions = document.querySelectorAll('.role-option');
        const roleInput = document.getElementById('role');
        const serenityBtn = document.getElementById('serenityBtn');
        
        // 显示注册区域
        function scrollToRegister() {
            const registerSection = document.getElementById('register');
            registerSection.scrollIntoView({ behavior: 'smooth' });
            
            // 滚动后稍微向上调整，避免被固定头部遮挡
            setTimeout(() => {
                window.scrollBy(0, -80);
            }, 500);
        }
        
        // 角色选择功能
        roleOptions.forEach(option => {
            option.addEventListener('click', function() {
                // 移除所有选项的选中状态
                roleOptions.forEach(opt => opt.classList.remove('selected'));
                
                // 添加当前选项的选中状态
                this.classList.add('selected');
                
                // 更新隐藏输入框的值
                roleInput.value = this.getAttribute('data-role');
            });
        });
        
        // 宁静守护模式模拟
        serenityBtn.addEventListener('click', function() {
            // 改变按钮状态
            const originalText = serenityBtn.innerHTML;
            serenityBtn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> 宁静模式启动中...';
            serenityBtn.disabled = true;
            
            // 模拟宁静模式体验
            setTimeout(() => {
                // 创建宁静模式全屏体验
                const serenityOverlay = document.createElement('div');
                serenityOverlay.style.cssText = `
                    position: fixed;
                    top: 0;
                    left: 0;
                    width: 100%;
                    height: 100%;
                    background: linear-gradient(135deg, #2a3a2f 0%, #3A4A3F 100%);
                    z-index: 2000;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                    color: white;
                    text-align: center;
                    padding: 20px;
                    font-family: "Microsoft YaHei", "微软雅黑", sans-serif;
                `;
                
                serenityOverlay.innerHTML = `
                    <div style="font-size: 2rem; margin-bottom: 30px; color: rgba(255,255,255,0.9); font-style: italic; font-weight: 300;">
                        <i class="fas fa-leaf" style="color: #8FB996; margin-right: 15px;"></i>
                        此刻，你肩上的重担，请暂时交给大地...
                    </div>
                    <div style="font-size: 1.2rem; margin-bottom: 40px; max-width: 600px; line-height: 1.8; color: rgba(255,255,255,0.7); font-weight: 300;">
                        深呼吸三次，感受身体与地球的连接。将眼前的救援场景，想象成人类共有的生命长河中的一瞬...
                    </div>
                    <div style="font-size: 1.4rem; margin: 40px 0; padding: 25px; border-top: 1px solid rgba(255,255,255,0.2); border-bottom: 1px solid rgba(255,255,255,0.2); width: 80%; max-width: 500px; color: #FAEDCA; font-weight: 300;">
                        "如果以百年后的目光回看此刻，你最想留下的是什么？"
                    </div>
                    <div style="display: flex; gap: 20px; margin-top: 30px;">
                        <button id="closeSerenity" style="background: #4A7C59; border: none; color: white; padding: 12px 30px; border-radius: 50px; font-size:
