<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Primus Mercearia - Qualidade e Sabor</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700&family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    
    <style>
        /* Variáveis de Cores e Estilo */
        :root {
            --cor-principal: #384F41; /* Verde Oliva Escuro */
            --cor-secundaria: #F0F0E8; /* Creme (Fundo) */
            --cor-destaque: #D1B000; /* Dourado/Amarelo Queimado */
            --cor-texto: #333;
            --cor-fundo-card: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--cor-secundaria);
            color: var(--cor-texto);
            line-height: 1.6;
        }

        /* HEADER & NAVEGAÇÃO */
        header {
            background-color: var(--cor-fundo-card);
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
            padding: 15px 5%;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
            font-size: 1.5rem;
            color: var(--cor-principal);
            text-decoration: none;
        }

        .nav-links a {
            color: var(--cor-principal);
            text-decoration: none;
            margin-left: 25px;
            font-weight: 600;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--cor-destaque);
        }

        /* HERO SECTION (Banner Principal) */
        .hero {
            background-image: url('https://images.unsplash.com/photo-1543781525-05566373809e?fit=crop&w=1400&q=80'); /* Imagem Placeholder Gourmet */
            background-size: cover;
            background-position: center;
            height: 500px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: var(--cor-secundaria); /* Texto Claro */
            position: relative;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.4); /* Overlay escuro */
        }

        .hero-content {
            position: relative;
            z-index: 10;
        }

        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 3rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }

        .btn-principal {
            background-color: var(--cor-destaque);
            color: var(--cor-principal);
            padding: 12px 30px;
            text-decoration: none;
            font-weight: 700;
            border-radius: 5px;
            transition: background-color 0.3s, transform 0.2s;
            display: inline-block;
        }

        .btn-principal:hover {
            background-color: #B89700; /* Tom mais escuro do dourado */
            transform: translateY(-2px);
        }

        /* SEÇÃO DE PRODUTOS */
        .section-produtos {
            padding: 60px 5%;
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }

        .section-produtos h2 {
            font-family: 'Montserrat', sans-serif;
            color: var(--cor-principal);
            margin-bottom: 40px;
            font-size: 2rem;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .card-produto {
            background-color: var(--cor-fundo-card);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
            text-align: left;
        }

        .card-produto:hover {
            transform: translateY(-5px);
        }

        .card-produto img {
            width: 100%;
            height: 200px;
            object-fit: cover;
            display: block;
        }

        .card-info {
            padding: 20px;
        }

        .card-info h3 {
            font-size: 1.25rem;
            color: var(--cor-principal);
            margin-bottom: 8px;
        }

        .card-info .preco {
            font-weight: 700;
            color: #C0392B; /* Preço em destaque (vermelho escuro) */
            font-size: 1.1rem;
        }

        /* RODAPÉ */
        footer {
            background-color: var(--cor-principal);
            color: var(--cor-secundaria);
            padding: 40px 5%;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            gap: 30px;
        }

        .footer-info h4 {
            font-family: 'Montserrat', sans-serif;
            margin-bottom: 15px;
            color: var(--cor-destaque);
            font-size: 1.2rem;
        }

        .footer-info p {
            margin-bottom: 8px;
            font-size: 0.9rem;
        }

        .social-icons a {
            color: var(--cor-secundaria);
            font-size: 1.5rem;
            margin-right: 15px;
            text-decoration: none;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: var(--cor-destaque);
        }

        /* RESPONSIVIDADE BÁSICA */
        @media (max-width: 768px) {
            .nav-links {
                display: none; /* Esconde menu para simplificar */
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .footer-content {
                justify-content: center;
                text-align: center;
            }

            .footer-info {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <header>
        <nav>
            <a href="#" class="logo">MP Primus Mercearia</a>
            <div class="nav-links">
                <a href="#produtos">Produtos</a>
                <a href="#kits">Kits</a>
                <a href="#ofertas">Ofertas</a>
                <a href="#contato">Contato</a>
                <a href="#" style="margin-left: 40px;">🛒 Carrinho (0)</a>
            </div>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>QUALIDADE E SABOR: DESDE 1990</h1>
            <a href="#produtos" class="btn-principal">VER PRODUTOS</a>
        </div>
    </section>

    <section class="section-produtos" id="produtos">
        <h2>Produtos Frescos e Selecionados</h2>
        
        <div class="product-grid">
            
            <div class="card-produto">
                <img src="https://images.unsplash.com/photo-1595167018873-1f810b42f74e?fit=crop&w=400&q=80" alt="Pão Artesanal">
                <div class="card-info">
                    <h3>Pão Artesanal</h3>
                    <p>Fresco, feito no dia.</p>
                    <p class="preco">R$ 12,99</p>
                </div>
            </div>

            <div class="card-produto">
                <img src="https://images.unsplash.com/photo-1586524673738-9e671c6d36e2?fit=crop&w=400&q=80" alt="Queijo Selecionado">
                <div class="card-info">
                    <h3>Queijo Minas (Aprox. 500g)</h3>
                    <p>Ideal para tábuas de frios.</p>
                    <p class="preco">R$ 38,50</p>
                </div>
            </div>
            
            <div class="card-produto">
                <img src="https://images.unsplash.com/photo-1582234032587-f82798e1003f?fit=crop&w=400&q=80" alt="Azeite">
                <div class="card-info">
                    <h3>Azeite Extra Virgem</h3>
                    <p>Importado, 500ml.</p>
                    <p class="preco">R$ 49,90</p>
                </div>
            </div>

            <div class="card-produto">
                <img src="https://images.unsplash.com/photo-1549419163-f2a890787e79?fit=crop&w=400&q=80" alt="Doce de Leite">
                <div class="card-info">
                    <h3>Doce de Leite Artesanal</h3>
                    <p>Pote de 400g.</p>
                    <p class="preco">R$ 22,00</p>
                </div>
            </div>

        </div>

    </section>
    
    <section class="section-produtos" id="kits" style="background-color: #EAEAE0; padding: 40px 5%;">
        <h2>Nossos Kits Especiais</h2>
        <div class="product-grid">
            <p style="grid-column: 1 / -1; font-style: italic; color: #555;">(Aqui entrariam os 3 Kits Especiais com imagens. Use esta seção para pedidos prontos.)</p>
        </div>
    </section>


    <footer id="contato">
        <div class="footer-content">
            
            <div class="footer-info">
                <h4>Localização</h4>
                <p>Rua dos Sabores, 123 - Centro</p>
                <p>Belo Horizonte / MG</p>
            </div>

            <div class="footer-info">
                <h4>Horário de Funcionamento</h4>
                <p>Segunda a Sábado: 08:00h - 19:00h</p>
                <p>Domingos: Fechado</p>
            </div>

            <div class="footer-info">
                <h4>Conecte-se</h4>
                <div class="social-icons">
                    <a href="https://wa.me/SEUNUMERO" target="_blank" title="Peça pelo WhatsApp">
                        <span style="font-size: 1.5rem;">&#x2709;</span> WhatsApp
                    </a>
                    <a href="https://instagram.com/SEUINSTAGRAM" target="_blank" title="Siga no Instagram">
                         <span style="font-size: 1.5rem;">&#x2764;</span> Instagram
                    </a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        console.log("Site da Primus Mercearia carregado com sucesso!");
    </script>

</body>
</html>
