<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Folder - Nutrição Esportiva e Clínica</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700;800&family=Playfair+Display:wght@700&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .folder-container {
            width: 100%;
            max-width: 800px;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
        }
        
        /* CAPA COM LOGO DE FUNDO */
        .cover {
            background: linear-gradient(135deg, rgba(46,204,113,0.95) 0%, rgba(39,174,96,0.95) 50%, rgba(52,152,219,0.95) 100%);
            padding: 100px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .cover::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 80%;
            height: 80%;
            background: url('/mnt/kimi/upload/Logotipo.png');
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
            opacity: 0.25;
            filter: blur(2px);
        }
        
        .cover-content {
            position: relative;
            z-index: 2;
        }
        
        .cover h1 {
            font-family: 'Playfair Display', serif;
            font-size: 56px;
            color: white;
            margin-bottom: 15px;
            text-shadow: 3px 3px 8px rgba(0,0,0,0.4);
            font-weight: 700;
            letter-spacing: 1px;
        }
        
        .cover .subtitle {
            font-size: 24px;
            color: rgba(255,255,255,0.95);
            font-weight: 300;
            letter-spacing: 5px;
            text-transform: uppercase;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        /* CONTEÚDO INTERNO */
        .content {
            padding: 50px 40px;
            background: linear-gradient(to bottom, #ffffff 0%, #f8f9fa 100%);
            position: relative;
        }
        
        /* BANNER DESTAQUE */
        .highlight-banner {
            background: linear-gradient(135deg, #2ecc71 0%, #27ae60 100%);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin: 20px 0 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .highlight-banner::before {
            content: '🏆 🏅 💪 ⚡ 🎯';
            font-size: 60px;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            opacity: 0.1;
            white-space: nowrap;
        }
        
        .highlight-banner h3 {
            font-size: 28px;
            margin-bottom: 15px;
            font-weight: 700;
            position: relative;
            z-index: 1;
        }
        
        .highlight-banner p {
            font-size: 18px;
            max-width: 500px;
            margin: 0 auto;
            opacity: 0.95;
            position: relative;
            z-index: 1;
        }
        
        /* ATENDIMENTOS */
        .section {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 32px;
            color: #2d3436;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            gap: 15px;
            text-align: center;
            justify-content: center;
        }
        
        .section-title .icon {
            font-size: 36px;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 25px;
            margin-top: 20px;
        }
        
        .service-box {
            background: white;
            border: 2px solid #e0e0e0;
            border-radius: 15px;
            padding: 35px 30px;
            text-align: center;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .service-box::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #2ecc71, #27ae60);
        }
        
        .service-box:hover {
            border-color: #2ecc71;
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(46, 204, 113, 0.2);
        }
        
        .service-box.sports::before {
            background: linear-gradient(90deg, #2ecc71, #27ae60);
        }
        
        .service-box.sports:hover {
            border-color: #2ecc71;
            box-shadow: 0 10px 30px rgba(46, 204, 113, 0.2);
        }
        
        .service-box .service-icon {
            font-size: 55px;
            margin-bottom: 20px;
            display: block;
        }
        
        .service-box h3 {
            font-size: 24px;
            color: #2d3436;
            margin-bottom: 20px;
            font-weight: 700;
        }
        
        .service-box ul {
            list-style: none;
            text-align: left;
            font-size: 15px;
            color: #636e72;
            line-height: 1.9;
            padding-left: 10px;
        }
        
        .service-box ul li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }
        
        .service-box ul li::before {
            content: '✓';
            position: absolute;
            left: 0;
            top: 0;
            color: #2ecc71;
            font-weight: bold;
            font-size: 18px;
        }
        
        .service-box.sports ul li::before {
            color: #2ecc71;
        }
        
        /* DIFERENCIAIS */
        .differentials {
            background: linear-gradient(135deg, #2d3436 0%, #1a1a2e 100%);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin: 40px 0;
            text-align: center;
        }
        
        .differentials h3 {
            font-size: 28px;
            margin-bottom: 25px;
            font-family: 'Playfair Display', serif;
        }
        
        .differentials-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        
        .differential-item {
            padding: 20px;
        }
        
        .differential-item .diff-icon {
            font-size: 40px;
            margin-bottom: 15px;
            display: block;
        }
        
        .differential-item p {
            font-size: 16px;
            line-height: 1.5;
            opacity: 0.9;
        }
        
        /* COMO FUNCIONA */
        .how-it-works {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            margin-top: 30px;
            text-align: center;
            gap: 20px;
        }
        
        .step {
            flex: 1;
            min-width: 140px;
            padding: 30px 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s;
            border-top: 4px solid #2ecc71;
        }
        
        .step:hover {
            transform: translateY(-5px);
        }
        
        .step:nth-child(2) { border-top-color: #27ae60; }
        .step:nth-child(3) { border-top-color: #2ecc71; }
        .step:nth-child(4) { border-top-color: #27ae60; }
        
        .step .step-icon {
            font-size: 45px;
            margin-bottom: 15px;
            display: block;
        }
        
        .step h4 {
            color: #2d3436;
            margin-bottom: 8px;
            font-size: 16px;
            font-weight: 700;
        }
        
        .step p {
            font-size: 13px;
            color: #636e72;
            line-height: 1.4;
        }
        
        /* CONTATO COM LOGO DE FUNDO */
        .contact-section {
            background: linear-gradient(135deg, #2d3436 0%, #1a1a2e 100%);
            color: white;
            padding: 70px 40px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .contact-section::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 60%;
            height: 60%;
            background: url('/mnt/kimi/upload/Logotipo.png');
            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;
            opacity: 0.08;
            filter: blur(1px);
        }
        
        .contact-content {
            position: relative;
            z-index: 2;
        }
        
        .contact-section h2 {
            font-family: 'Playfair Display', serif;
            font-size: 40px;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }
        
        .contact-section .cta {
            font-size: 19px;
            opacity: 0.9;
            margin-bottom: 40px;
            font-weight: 300;
        }
        
        .contact-grid {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
            margin-bottom: 40px;
        }
        
        .contact-item {
            background: rgba(255,255,255,0.1);
            padding: 25px 30px;
            border-radius: 15px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            transition: all 0.3s;
            min-width: 220px;
        }
        
        .contact-item:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-5px);
        }
        
        .contact-item .label {
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 2px;
            opacity: 0.7;
            margin-bottom: 8px;
        }
        
        .contact-item .value {
            font-size: 17px;
            font-weight: 600;
        }
        
        .btn-whatsapp {
            display: inline-block;
            background: #25D366;
            color: white;
            text-decoration: none;
            padding: 22px 55px;
            border-radius: 50px;
            font-weight: 700;
            font-size: 20px;
            transition: all 0.3s;
            box-shadow: 0 6px 20px rgba(37, 211, 102, 0.4);
            margin-top: 10px;
        }
        
        .btn-whatsapp:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(37, 211, 102, 0.6);
        }
        
        /* RESPONSIVO */
        @media (max-width: 600px) {
            .cover h1 { font-size: 40px; }
            .cover { padding: 80px 20px; }
            .cover::before { width: 95%; height: 95%; }
            .services-grid { grid-template-columns: 1fr; }
            .content { padding: 30px 20px; }
            .contact-item { min-width: 100%; }
            .how-it-works { flex-direction: column; }
            .contact-section::before { width: 90%; height: 90%; }
            .differentials-grid { grid-template-columns: 1fr; }
        }
        
        /* PRINT OPTIMIZATION */
        @media print {
            body { background: white; }
            .folder-container { box-shadow: none; }
            .service-box, .step { break-inside: avoid; }
        }
    </style>
</head>
<body>
    <div class="folder-container">
        <!-- CAPA COM LOGO DE FUNDO -->
        <div class="cover">
            <div class="cover-content">
                <h1>Nutrição que Performa</h1>
                <p class="subtitle">Esportiva & Clínica</p>
            </div>
        </div>
        
        <!-- CONTEÚDO -->
        <div class="content">
            <!-- BANNER DESTAQUE -->
            <div class="highlight-banner">
                <h3>🏆 Atleta e Nutricionista</h3>
                <p>Entendo na prática as necessidades do seu corpo para entregar resultados reais</p>
            </div>
            
            <!-- ATENDIMENTOS -->
            <div class="section">
                <h2 class="section-title">
                    <span class="icon">📋</span>
                    Atendimentos
                </h2>
                
                <div class="services-grid">
                    <div class="service-box clinical">
                        <span class="service-icon">🩺</span>
                        <h3>Nutrição Clínica</h3>
                        <ul>
                            <li>Avaliação antropométrica completa</li>
                            <li>Planejamento alimentar terapêutico</li>
                            <li>Controle de doenças crônicas</li>
                            <li>Reeducação alimentar</li>
                            <li>Emagrecimento saudável</li>
                        </ul>
                    </div>
                    <div class="service-box sports">
                        <span class="service-icon">🏆</span>
                        <h3>Nutrição Esportiva</h3>
                        <ul>
                            <li>Periodização nutricional</li>
                            <li>Estratégia para competições</li>
                            <li>Suplementação esportiva</li>
                            <li>Composição corporal</li>
                            <li>Recuperação muscular</li>
                        </ul>
                    </div>
                </div>
            </div>
            
            <!-- DIFERENCIAIS -->
            <div class="differentials">
                <h3>🌟 Meus Diferenciais</h3>
                <div class="differentials-grid">
                    <div class="differential-item">
                        <span class="diff-icon">🎯</span>
                        <p>Experiência prática como atleta de múltiplos esportes</p>
                    </div>
                    <div class="differential-item">
                        <span class="diff-icon">📊</span>
                        <p>Protocolos baseados em evidências científicas</p>
                    </div>
                    <div class="differential-item">
                        <span class="diff-icon">🤝</span>
                        <p>Acompanhamento próximo e ajustes personalizados</p>
                    </div>
                </div>
            </div>
            
            <!-- COMO FUNCIONA -->
            <div class="section">
                <h2 class="section-title">
                    <span class="icon">🔄</span>
                    Como Funciona
                </h2>
                <div class="how-it-works">
                    <div class="step">
                        <span class="step-icon">📱</span>
                        <h4>1. Contato</h4>
                        <p>Agende sua consulta pelo WhatsApp</p>
                    </div>
                    <div class="step">
                        <span class="step-icon">📊</span>
                        <h4>2. Avaliação</h4>
                        <p>Análise completa do seu perfil e objetivos</p>
                    </div>
                    <div class="step">
                        <span class="step-icon">📋</span>
                        <h4>3. Plano</h4>
                        <p>Prescrição 100% personalizada</p>
                    </div>
                    <div class="step">
                        <span class="step-icon">🤝</span>
                        <h4>4. Acompanhamento</h4>
                        <p>Suporte contínuo e ajustes semanais</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- CONTATO COM LOGO DE FUNDO -->
        <div class="contact-section">
            <div class="contact-content">
                <h2>Vamos Começar?</h2>
                <p class="cta">Sua jornada para uma nutrição de alto performance começa agora.</p>
                
                <div class="contact-grid">
                    <div class="contact-item">
                        <div class="label">WhatsApp</div>
                        <div class="value">(61) 98196-1802</div>
                    </div>
                    <div class="contact-item">
                        <div class="label">Instagram</div>
                        <div class="value">@helio_escaleira</div>
                    </div>
                    <div class="contact-item">
                        <div class="label">Email</div>
                        <div class="value">nutri.escaleira@gmail.com</div>
                    </div>
                </div>
                
                <a href="https://wa.me/5561981961802" class="btn-whatsapp" target="_blank">
                    💬 Agendar Consulta
                </a>
            </div>
        </div>
    </div>
</body>
</html>
