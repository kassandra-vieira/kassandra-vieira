<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Alex Morgan · Perfil GitHub Dev</title>
    <!-- Google Fonts + Font Awesome 6 (free) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700;14..32,800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: radial-gradient(circle at 10% 20%, #0B0F1C, #03050A);
            font-family: 'Inter', sans-serif;
            color: #eef2ff;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        /* vívido brilho de fundo */
        .bg-glow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
            background: radial-gradient(ellipse at 40% 50%, rgba(56, 139, 253, 0.08), transparent 70%);
        }

        .container {
            max-width: 1280px;
            margin: 0 auto;
            padding: 2rem 1.5rem 4rem;
            position: relative;
            z-index: 2;
        }

        /* header / avatar + nome */
        .hero {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 2rem;
            margin-bottom: 3rem;
            backdrop-filter: blur(2px);
        }

        .hero-info {
            display: flex;
            align-items: center;
            gap: 1.8rem;
            flex-wrap: wrap;
        }

        .avatar-frame {
            background: linear-gradient(135deg, #388bfd, #8b5cf6, #ec489a);
            padding: 3px;
            border-radius: 50%;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.5), 0 0 0 1px rgba(255, 255, 255, 0.05);
            transition: transform 0.2s ease;
        }

        .avatar-frame:hover {
            transform: scale(1.02);
        }

        .avatar {
            width: 110px;
            height: 110px;
            border-radius: 50%;
            object-fit: cover;
            background: #1e2436;
            display: block;
        }

        .name-section h1 {
            font-size: 2.5rem;
            font-weight: 700;
            background: linear-gradient(to right, #ffffff, #c0d9ff);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.02em;
        }

        .badge {
            background: rgba(56, 139, 253, 0.2);
            backdrop-filter: blur(4px);
            padding: 0.3rem 0.9rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            border: 1px solid rgba(56, 139, 253, 0.4);
            display: inline-flex;
            align-items: center;
            gap: 6px;
            margin-top: 8px;
        }

        .badge i {
            font-size: 0.7rem;
            color: #58a6ff;
        }

        .hero-stats {
            display: flex;
            gap: 2rem;
            background: rgba(18, 25, 45, 0.5);
            backdrop-filter: blur(8px);
            padding: 0.8rem 1.8rem;
            border-radius: 60px;
            border: 1px solid rgba(72, 110, 170, 0.3);
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-weight: 800;
            font-size: 1.6rem;
            line-height: 1;
            background: linear-gradient(135deg, #f0f4ff, #b3cdff);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .stat-label {
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            color: #9aa9c1;
        }

        /* bio card moderna */
        .bio-card {
            background: rgba(12, 18, 30, 0.65);
            backdrop-filter: blur(12px);
            border-radius: 2rem;
            padding: 1.8rem 2rem;
            margin-bottom: 2.5rem;
            border: 1px solid rgba(72, 110, 170, 0.25);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            transition: all 0.2s;
        }

        .bio-text {
            font-size: 1.1rem;
            font-weight: 400;
            color: #cddcff;
            display: flex;
            align-items: flex-start;
            gap: 12px;
        }

        .bio-text i {
            font-size: 1.6rem;
            color: #388bfd;
            margin-top: 2px;
        }

        .location {
            margin-top: 1rem;
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            font-size: 0.85rem;
            color: #8d9ccd;
        }

        .location span i {
            margin-right: 5px;
            width: 18px;
        }

        /* grid de projetos / repos moderno */
        .section-title {
            display: flex;
            align-items: baseline;
            justify-content: space-between;
            margin: 2rem 0 1.2rem 0;
            flex-wrap: wrap;
        }

        .section-title h2 {
            font-weight: 600;
            font-size: 1.7rem;
            letter-spacing: -0.3px;
            background: linear-gradient(to right, #eef2ff, #99bbff);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }

        .github-link {
            background: #1f2a44;
            padding: 0.4rem 1rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            transition: 0.2s;
            text-decoration: none;
            color: #c9dcff;
        }

        .github-link i {
            margin-right: 6px;
        }

        .github-link:hover {
            background: #2f3b60;
            color: white;
        }

        .repo-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.8rem;
            margin-top: 0.5rem;
        }

        .repo-card {
            background: rgba(18, 24, 41, 0.7);
            backdrop-filter: blur(8px);
            border-radius: 1.6rem;
            padding: 1.5rem;
            border: 1px solid rgba(72, 110, 170, 0.2);
            transition: all 0.25s ease;
            box-shadow: 0 8px 18px rgba(0, 0, 0, 0.2);
        }

        .repo-card:hover {
            transform: translateY(-5px);
            border-color: rgba(56, 139, 253, 0.5);
            background: rgba(24, 32, 55, 0.8);
            box-shadow: 0 20px 30px -12px rgba(0, 0, 0, 0.4);
        }

        .repo-name {
            font-weight: 700;
            font-size: 1.25rem;
            display: flex;
            align-items: center;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 0.6rem;
        }

        .repo-name i {
            color: #58a6ff;
            font-size: 1.1rem;
        }

        .repo-desc {
            font-size: 0.85rem;
            color: #b2c2e6;
            margin: 0.6rem 0 0.9rem 0;
            line-height: 1.4;
        }

        .repo-meta {
            display: flex;
            gap: 1rem;
            font-size: 0.7rem;
            font-weight: 500;
            color: #8d9fd3;
        }

        .repo-meta span i {
            margin-right: 4px;
        }

        .lang-badge {
            background: #1e2a47;
            padding: 0.2rem 0.6rem;
            border-radius: 20px;
            font-size: 0.7rem;
            font-weight: 600;
            color: #b9d0ff;
        }

        /* skills & tech stack */
        .skills-wrapper {
            margin: 2rem 0 2rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 1rem;
        }

        .skill-tag {
            background: rgba(56, 139, 253, 0.12);
            border: 1px solid rgba(56, 139, 253, 0.3);
            padding: 0.5rem 1rem;
            border-radius: 60px;
            font-size: 0.8rem;
            font-weight: 500;
            transition: 0.1s;
            backdrop-filter: blur(4px);
        }

        .skill-tag i {
            margin-right: 6px;
            font-size: 0.8rem;
        }

        /* social links row */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: flex-start;
            gap: 1.2rem;
            margin-top: 2.2rem;
            border-top: 1px solid rgba(72, 110, 170, 0.3);
            padding-top: 2rem;
        }

        .social-icon {
            background: rgba(28, 35, 58, 0.8);
            backdrop-filter: blur(5px);
            width: 44px;
            height: 44px;
            border-radius: 30px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            color: #bdd3ff;
            transition: all 0.2s;
            text-decoration: none;
        }

        .social-icon:hover {
            background: #388bfd;
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px -5px #388bfd50;
        }

        /* footer */
        .footer-note {
            text-align: center;
            margin-top: 3rem;
            font-size: 0.75rem;
            color: #5a6e97;
        }

        /* responsividade */
        @media (max-width: 720px) {
            .hero {
                flex-direction: column;
                align-items: flex-start;
            }
            .hero-stats {
                width: 100%;
                justify-content: space-between;
            }
            .name-section h1 {
                font-size: 2rem;
            }
            .bio-card {
                padding: 1.3rem;
            }
        }

        /* animação suave de entrada */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(18px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero, .bio-card, .repo-card, .skills-wrapper, .social-links {
            animation: fadeUp 0.5s ease backwards;
        }

        .hero { animation-delay: 0.05s; }
        .bio-card { animation-delay: 0.1s; }
        .repo-card:nth-child(1) { animation-delay: 0.15s; }
        .repo-card:nth-child(2) { animation-delay: 0.2s; }
        .repo-card:nth-child(3) { animation-delay: 0.25s; }
        .skills-wrapper { animation-delay: 0.3s; }
        .social-links { animation-delay: 0.35s; }
    </style>
</head>
<body>
<div class="bg-glow"></div>
<div class="container">
    <!-- Seção hero com avatar e estatísticas -->
    <div class="hero">
        <div class="hero-info">
            <div class="avatar-frame">
                <img class="avatar" src="https://ui-avatars.com/api/?background=1E293B&color=388bfd&bold=true&size=110&name=Alex+Morgan&length=2&fontsize=0.55&rounded=true" alt="Avatar Alex Morgan">
            </div>
            <div class="name-section">
                <h1>Alex Morgan</h1>
                <div class="badge">
                    <i class="fab fa-github"></i> @alexmorgan · Full Stack Architect
                </div>
                <div class="badge" style="background: rgba(139, 92, 246, 0.15); border-color: #8b5cf670;">
                    <i class="fas fa-map-marker-alt"></i> Remote · Berlin, DE
                </div>
            </div>
        </div>
        <div class="hero-stats">
            <div class="stat">
                <div class="stat-number">48</div>
                <div class="stat-label">repositórios</div>
            </div>
            <div class="stat">
                <div class="stat-number">2.3k</div>
                <div class="stat-label">seguidores</div>
            </div>
            <div class="stat">
                <div class="stat-number">32</div>
                <div class="stat-label">contribuições</div>
            </div>
        </div>
    </div>

    <!-- Bio card com introdução e localização extra -->
    <div class="bio-card">
        <div class="bio-text">
            <i class="fas fa-quote-left"></i>
            <span>Arquiteto de software e criador de experiências digitais escaláveis. Apaixonado por open source, cloud native e design systems. Transformo ideias em código limpo e performático.</span>
        </div>
        <div class="location">
            <span><i class="fas fa-briefcase"></i> Tech Lead @ NebulaSoft</span>
            <span><i class="fas fa-graduation-cap"></i> M.Sc. Computer Science</span>
            <span><i class="fas fa-code-branch"></i> 8+ anos de experiência</span>
        </div>
    </div>

    <!-- Projetos em destaque / repositórios modernos -->
    <div class="section-title">
        <h2><i class="fab fa-github" style="margin-right: 8px;"></i> Projetos em destaque</h2>
        <a href="#" class="github-link"><i class="fab fa-github"></i> ver todos os repositórios →</a>
    </div>

    <div class="repo-grid">
        <!-- card 1 -->
        <div class="repo-card">
            <div class="repo-name">
                <i class="fab fa-react"></i> astra-ui
                <span class="lang-badge">TypeScript</span>
            </div>
            <div class="repo-desc">
                Biblioteca de componentes React moderna e acessível com tema dinâmico, animações fluidas e documentação interativa.
            </div>
            <div class="repo-meta">
                <span><i class="fas fa-star"></i> 847</span>
                <span><i class="fas fa-code-branch"></i> 124</span>
                <span><i class="fas fa-clock"></i> atualizado há 2 dias</span>
            </div>
        </div>
        <!-- card 2 -->
        <div class="repo-card">
            <div class="repo-name">
                <i class="fab fa-node-js"></i> nebula-api
                <span class="lang-badge">Node.js</span>
            </div>
            <div class="repo-desc">
                Backend GraphQL com NestJS, Prisma ORM, autenticação JWT e deploy em Kubernetes. Altamente performático.
            </div>
            <div class="repo-meta">
                <span><i class="fas fa-star"></i> 1.2k</span>
                <span><i class="fas fa-code-branch"></i> 205</span>
                <span><i class="fas fa-clock"></i> atualizado há 1 semana</span>
            </div>
        </div>
        <!-- card 3 -->
        <div class="repo-card">
            <div class="repo-name">
                <i class="fab fa-python"></i> ml-observability
                <span class="lang-badge">Python</span>
            </div>
            <div class="repo-desc">
                Framework para monitoramento de modelos de ML, drift detection e explicabilidade com visualizações em tempo real.
            </div>
            <div class="repo-meta">
                <span><i class="fas fa-star"></i> 562</span>
                <span><i class="fas fa-code-branch"></i> 78</span>
                <span><i class="fas fa-clock"></i> atualizado há 4 dias</span>
            </div>
        </div>
        <!-- card 4 extra -->
        <div class="repo-card">
            <div class="repo-name">
                <i class="fas fa-cloud"></i> terraform-aws-modules
                <span class="lang-badge">HCL</span>
            </div>
            <div class="repo-desc">
                Módulos Terraform reutilizáveis para infraestrutura AWS (EKS, RDS, VPC) com boas práticas de segurança.
            </div>
            <div class="repo-meta">
                <span><i class="fas fa-star"></i> 401</span>
                <span><i class="fas fa-code-branch"></i> 32</span>
                <span><i class="fas fa-clock"></i> atualizado há 3 semanas</span>
            </div>
        </div>
    </div>

    <!-- Tecnologias & Skills -->
    <div class="skills-wrapper">
        <div class="section-title" style="margin-bottom: 0.5rem;">
            <h2><i class="fas fa-cogs"></i> Tech Stack & Ferramentas</h2>
        </div>
        <div class="skill-tags">
            <span class="skill-tag"><i class="fab fa-react"></i> React</span>
            <span class="skill-tag"><i class="fab fa-vuejs"></i> Vue 3</span>
            <span class="skill-tag"><i class="fab fa-node-js"></i> Node.js</span>
            <span class="skill-tag"><i class="fab fa-python"></i> Python</span>
            <span class="skill-tag"><i class="fab fa-go"></i> Golang</span>
            <span class="skill-tag"><i class="fas fa-database"></i> PostgreSQL</span>
            <span class="skill-tag"><i class="fab fa-docker"></i> Docker</span>
            <span class="skill-tag"><i class="fab fa-kubernetes"></i> K8s</span>
            <span class="skill-tag"><i class="fab fa-aws"></i> AWS</span>
            <span class="skill-tag"><i class="fas fa-code"></i> GraphQL</span>
            <span class="skill-tag"><i class="fab fa-github"></i> GitHub Actions</span>
        </div>
    </div>

    <!-- Atividade e GitHub stats minicard -->
    <div class="bio-card" style="margin-top: 0.2rem; padding: 1.4rem 1.8rem;">
        <div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 1rem;">
            <div>
                <i class="fas fa-chart-line" style="color: #58a6ff; margin-right: 6px;"></i>
                <strong>Contribuições recentes:</strong> 412 commits nos últimos 30 dias
            </div>
            <div style="display: flex; gap: 12px;">
                <span><i class="fas fa-trophy"></i> GitHub Star 2024</span>
                <span><i class="fas fa-certificate"></i> Cloud Architect Certified</span>
            </div>
        </div>
        <div style="margin-top: 14px; background: #0A0F1C; border-radius: 50px; height: 6px; width: 100%; overflow: hidden;">
            <div style="width: 78%; background: linear-gradient(90deg, #388bfd, #a855f7); height: 6px; border-radius: 50px;"></div>
        </div>
        <div style="display: flex; justify-content: space-between; font-size: 0.7rem; margin-top: 8px;">
            <span>🔥 78% atividade este mês</span>
            <span><i class="fas fa-calendar-alt"></i> 12 dias consecutivos de código</span>
        </div>
    </div>

    <!-- Redes sociais / contato profissional -->
    <div class="social-links">
        <a href="#" class="social-icon" aria-label="GitHub"><i class="fab fa-github"></i></a>
        <a href="#" class="social-icon" aria-label="LinkedIn"><i class="fab fa-linkedin-in"></i></a>
        <a href="#" class="social-icon" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
        <a href="#" class="social-icon" aria-label="Dev.to"><i class="fab fa-dev"></i></a>
        <a href="#" class="social-icon" aria-label="Email"><i class="fas fa-envelope"></i></a>
        <a href="#" class="social-icon" aria-label="Discord"><i class="fab fa-discord"></i></a>
    </div>

    <!-- footer com contribuição sutil -->
    <div class="footer-note">
        <i class="fas fa-code"></i> com ♥ para a comunidade open source · disponível para colaborações
    </div>
</div>
</body>
</html>
