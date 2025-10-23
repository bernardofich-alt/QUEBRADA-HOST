<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quebrada HOST - Conectando Mundos na Periferia</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --roxo-principal: #6A1B9A; /* Um roxo vibrante */
            --roxo-claro: #E0BEE0;
            --verde-destaque: #8BC34A; /* Para botões de ação */
            --cinza-texto: #333;
            --branco: #fff;
            --sombra-leve: rgba(0, 0, 0, 0.1);
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: var(--cinza-texto);
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Cabeçalho */
        header {
            background-color: var(--roxo-principal);
            color: var(--branco);
            padding: 1rem 0;
            text-align: center;
            box-shadow: 0 2px 4px var(--sombra-leve);
        }

        header h1 {
            margin: 0;
            font-size: 2.5rem;
            letter-spacing: 1px;
        }

        header p {
            font-size: 1.1rem;
            margin-top: 5px;
            opacity: 0.9;
        }

        /* Navegação */
        nav ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
            margin-top: 15px;
        }

        nav ul li {
            margin: 0 15px;
        }

        nav ul li a {
            color: var(--branco);
            text-decoration: none;
            font-weight: 600;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: var(--roxo-claro);
        }

        /* Seção Herói */
        .hero {
            background: linear-gradient(rgba(106, 27, 154, 0.8), rgba(106, 27, 154, 0.8)), url('https://via.placeholder.com/1500x500/6A1B9A/FFFFFF?text=Imagem+da+Periferia+Vibrante') no-repeat center center/cover;
            color: var(--branco);
            text-align: center;
            padding: 80px 20px;
            animation: fadeIn 1s ease-out;
        }

        .hero h2 {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.3rem;
            max-width: 800px;
            margin: 0 auto 30px auto;
        }

        .btn {
            background-color: var(--verde-destaque);
            color: var(--branco);
            padding: 15px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 1.1rem;
            transition: background-color 0.3s ease, transform 0.2s ease;
            display: inline-block;
            margin: 10px;
        }

        .btn:hover {
            background-color: #7CB342; /* Um verde um pouco mais escuro */
            transform: translateY(-3px);
            box-shadow: 0 4px 8px var(--sombra-leve);
        }

        /* Seções de Conteúdo */
        .section-title {
            text-align: center;
            font-size: 2.2rem;
            color: var(--roxo-principal);
            margin-bottom: 40px;
            position: relative;
            padding-bottom: 10px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--verde-destaque);
            border-radius: 2px;
        }

        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .card {
            background-color: var(--branco);
            border-radius: 10px;
            box-shadow: 0 4px 15px var(--sombra-leve);
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 8px 20px var(--sombra-leve);
        }

        .card h3 {
            color: var(--roxo-principal);
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .card p {
            font-size: 1rem;
            color: #555;
        }

        .icon {
            font-size: 3rem;
            color: var(--verde-destaque);
            margin-bottom: 20px;
        }

        /* Seção Parceiros */
        .parceiros-logo {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            gap: 40px;
            margin-top: 40px;
        }

        .parceiros-logo img {
            max-width: 150px;
            height: auto;
            filter: grayscale(80%);
            opacity: 0.7;
            transition: all 0.3s ease;
        }

        .parceiros-logo img:hover {
            filter: grayscale(0%);
            opacity: 1;
            transform: scale(1.05);
        }

        /* Depoimentos */
        .depoimento {
            background-color: var(--branco);
            border-radius: 10px;
            box-shadow: 0 4px 15px var(--sombra-leve);
            padding: 30px;
            margin-bottom: 30px;
            text-align: center;
            font-style: italic;
        }

        .depoimento p {
            font-size: 1.1rem;
            color: #444;
            margin-bottom: 15px;
        }

        .depoimento .autor {
            font-weight: 600;
            color: var(--roxo-principal);
            font-style: normal;
        }

        /* Rodapé */
        footer {
            background-color: var(--roxo-principal);
            color: var(--branco);
            text-align: center;
            padding: 40px 20px;
            margin-top: 60px;
            box-shadow: 0 -2px 4px var(--sombra-leve);
        }

        footer .social-icons a {
            color: var(--branco);
            font-size: 1.8rem;
            margin: 0 10px;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        footer .social-icons a:hover {
            color: var(--roxo-claro);
        }

        footer p {
            margin-top: 20px;
            font-size: 0.9rem;
        }

        /* Animações */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Font Awesome para ícones (opcional, mas recomendado) */
        .fa-globe-americas:before { content: "\f572"; } /* Exemplo de ícone */
        .fa-language:before { content: "\f1ab"; }
        .fa-money-bill-wave:before { content: "\f53a"; }
        .fa-handshake:before { content: "\f2b5"; }
        .fa-facebook:before { content: "\f09a"; }
        .fa-instagram:before { content: "\f16d"; }
        .fa-whatsapp:before { content: "\f232"; }

        /* Você precisaria linkar o Font Awesome no <head> se quiser usá-los de verdade: */
        /* <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"> */

    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Quebrada HOST</h1>
            <p>Seu Anfitrião na Periferia</p>
            <nav>
                <ul>
                    <li><a href="#sobre">Sobre Nós</a></li>
                    <li><a href="#como-funciona">Como Funciona</a></li>
                    <li><a href="#para-turistas">Para Turistas</a></li>
                    <li><a href="#para-hosts">Para Hosts</a></li>
                    <li><a href="#parceiros">Parceiros</a></li>
                    <li><a href="#contato">Contato</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero">
            <div class="container">
                <h2>Conecte-se, Explore e Viva a Autenticidade da Periferia com o Quebrada HOST</h2>
                <p>Descubra a riqueza cultural das nossas comunidades com anfitriões locais, pratique idiomas e desfrute de experiências autênticas, apoiando o desenvolvimento local.</p>
                <a href="#para-turistas" class="btn">Sou Turista!</a>
                <a href="#para-hosts" class="btn">Quero Ser HOST!</a>
            </div>
        </section>

        <section id="sobre" class="container" style="padding: 60px 20px;">
            <h2 class="section-title">Nossa Missão</h2>
            <div class="card-grid">
                <div class="card">
                    <span class="icon">&#127760;</span> <h3>Conexão Humana</h3>
                    <p>Facilitar a troca cultural genuína entre turistas e os hosts da periferia, quebrando barreiras e promovendo a inclusão.</p>
                </div>
                <div class="card">
                    <span class="icon">&#128172;</span> <h3>Aprendizado Mútuo</h3>
                    <p>Oferecer aos nossos hosts a chance de praticar idiomas e aos turistas uma imersão linguística e cultural.</p>
                </div>
                <div class="card">
                    <span class="icon">&#128184;</span> <h3>Empoderamento Local</h3>
                    <p>Criar uma fonte de renda sustentável e valorizar o conhecimento e a hospitalidade dos moradores locais.</p>
                </div>
            </div>
        </section>

        <section id="como-funciona" class="container" style="padding: 60px 20px; background-color: var(--roxo-claro);">
            <h2 class="section-title">Como o Quebrada HOST Funciona</h2>
            <div class="card-grid">
                <div class="card">
                    <span class="icon">&#128100;</span> <h3>1. Seja um HOST</h3>
                    <p>Moradores interessados em ser anfitriões se cadastram em nossa plataforma e recebem suporte para criar suas experiências.</p>
                </div>
                <div class="card">
                    <span class="icon">&#128171;</span> <h3>2. Escolha sua Aventura</h3>
                    <p>Turistas exploram os perfis dos hosts e selecionam as experiências que mais combinam com seus interesses e curiosidades.</p>
                </div>
                <div class="card">
                    <span class="icon">&#128205;</span> <h3>3. Conecte-se e Explore</h3>
                    <p>HOST e turista se encontram para uma imersão cultural, praticam idiomas e aproveitam a culinária e os pontos locais com nossos parceiros.</p>
                </div>
                <div class="card">
                    <span class="icon">&#128176;</span> <h3>4. Impacto Real</h3>
                    <p>Os hosts recebem comissões pelas experiências, e nossos parceiros locais ganham visibilidade e movimento, impulsionando a economia da quebrada.</p>
                </div>
            </div>
        </section>

        <section id="para-turistas" class="container" style="padding: 60px 20px;">
            <h2 class="section-title">Para Turistas: Sua Próxima Grande Experiência</h2>
            <p style="text-align: center; font-size: 1.1rem; max-width: 800px; margin: 0 auto 40px auto;">
                Prepare-se para ir além do óbvio. Com o Quebrada HOST, sua viagem se transforma em uma jornada de descobertas e conexões verdadeiras.
            </p>
            <div class="card-grid">
                <div class="card">
                    <h3>Vivências Inesquecíveis</h3>
                    <p>Descubra a cultura local através dos olhos de quem a vive, com histórias e sabores que só a quebrada oferece.</p>
                </div>
                <div class="card">
                    <h3>Troca de Idiomas</h3>
                    <p>Aprimore seu português (ou ensine o seu idioma!) em conversas autênticas e descontraídas com pessoas locais.</p>
                </div>
                <div class="card">
                    <h3>Turismo de Impacto</h3>
                    <p>Cada experiência contribui diretamente para o desenvolvimento econômico e o empoderamento das comunidades visitadas.</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 50px;">
                <a href="#" class="btn">Encontre Seu HOST</a>
            </div>
        </section>

        <section id="para-hosts" class="container" style="padding: 60px 20px; background-color: var(--roxo-claro);">
            <h2 class="section-title">Para HOSTS: Compartilhe Sua Quebrada, Conecte Mundos</h2>
            <p style="text-align: center; font-size: 1.1rem; max-width: 800px; margin: 0 auto 40px auto;">
                Você tem histórias, cultura e hospitalidade para oferecer. Torne-se um HOST e seja um embaixador da sua comunidade!
            </p>
            <div class="card-grid">
                <div class="card">
                    <h3>Gere Renda</h3>
                    <p>Transforme seu tempo e conhecimento em uma remuneração justa, recebendo comissões por suas experiências.</p>
                </div>
                <div class="card">
                    <h3>Desenvolvimento Pessoal</h3>
                    <p>Pratique e aprimore seus idiomas, conheça novas culturas e amplie sua rede de contatos globais.</p>
                </div>
                <div class="card">
                    <h3>Valorize Sua Quebrada</h3>
                    <p>Mostre o melhor da sua comunidade, desconstruindo estereótipos e promovendo o orgulho local.</p>
                </div>
            </div>
            <div style="text-align: center; margin-top: 50px;">
                <a href="#" class="btn">Quero Ser HOST!</a>
            </div>
        </section>

        <section id="parceiros" class="container" style="padding: 60px 20px;">
            <h2 class="section-title">Nossos Parceiros Locais</h2>
            <p style="text-align: center; font-size: 1.1rem; max-width: 800px; margin: 0 auto 40px auto;">
                Uma rede de estabelecimentos acolhedores que, junto com o Quebrada HOST, oferecem o melhor da nossa comunidade.
            </p>
            <div class="parceiros-logo">
                <img src="https://via.placeholder.com/150x80/E0BEE0/6A1B9A?text=Boteco+do+Zé" alt="Logo Boteco do Zé">
                <img src="https://via.placeholder.com/150x80/E0BEE0/6A1B9A?text=Feira+Cultural" alt="Logo Feira Cultural">
                <img src="https://via.placeholder.com/150x80/E0BEE0/6A1B9A?text=Grafitti+Tour" alt="Logo Grafitti Tour">
                <img src="https://via.placeholder.com/150x80/E0BEE0/6A1B9A?text=Pizzaria+Da+Hora" alt="Logo Pizzaria Da Hora">
            </div>
            <div style="text-align: center; margin-top: 50px;">
                <a href="#" class="btn">Seja um Parceiro!</a>
            </div>
        </section>

        <section id="depoimentos" class="container" style="padding: 60px 20px; background-color: #fcfcfc;">
            <h2 class="section-title">O Que Dizem Sobre o Quebrada HOST</h2>
            <div class="card-grid">
                <div class="depoimento">
                    <p>"Minha experiência com a Quebrada HOST foi transformadora. Conheci pessoas incríveis, provei a verdadeira culinária local e aprendi muito sobre a cultura brasileira. Uma viagem que foi muito além do turismo comum."</p>
                    <p class="autor">- Emma (Canadá), Turista</p>
                </div>
                <div class="depoimento">
                    <p>"Ser HOST me deu uma nova perspectiva. Tenho a oportunidade de mostrar a beleza e a potência da minha quebrada, além de praticar meu inglês e fazer um dinheiro extra. É gratificante!"</p>
                    <p class="autor">- Marcos (Heliópolis), HOST Local</p>
                </div>
                <div class="depoimento">
                    <p>"Nosso bar sempre foi um ponto de encontro, e com a Quebrada HOST, recebemos gente do mundo todo! É uma alegria ver a periferia sendo valorizada e movimentada de um jeito tão positivo."</p>
                    <p class="autor">- Dona Lúcia (Bar & Petiscos), Parceira</p>
                </div>
            </div>
        </section>

        <section id="contato" class="container" style="padding: 60px 20px;">
            <h2 class="section-title">Fale Conosco</h2>
            <p style="text-align: center; max-width: 600px; margin: 0 auto 40px auto;">
                Tem alguma dúvida, quer dar uma sugestão ou deseja fazer parte da família Quebrada HOST? Estamos aqui para você!
            </p>
            <form style="max-width: 600px; margin: 0 auto; background-color: var(--branco); padding: 30px; border-radius: 10px; box-shadow: 0 4px 15px var(--sombra-leve);">
                <div style="margin-bottom: 20px;">
                    <label for="nome" style="display: block; margin-bottom: 8px; font-weight: 600;">Seu Nome:</label>
                    <input type="text" id="nome" name="nome" required style="width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 5px; box-sizing: border-box;">
                </div>
                <div style="margin-bottom: 20px;">
                    <label for="email" style="display: block; margin-bottom: 8px; font-weight: 600;">Seu E-mail:</label>
                    <input type="email" id="email" name="email" required style="width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 5px; box-sizing: border-box;">
                </div>
                <div style="margin-bottom: 20px;">
                    <label for="mensagem" style="display: block; margin-bottom: 8px; font-weight: 600;">Sua Mensagem:</label>
                    <textarea id="mensagem" name="mensagem" rows="6" required style="width: 100%; padding: 12px; border: 1px solid #ddd; border-radius: 5px; box-sizing: border-box; resize: vertical;"></textarea>
                </div>
                <button type="submit" class="btn" style="width: 100%; border: none; cursor: pointer;">Enviar Mensagem</button>
            </form>
        </section>

    </main>

    <footer>
        <div class="container">
            <div class="social-icons">
                <a href="#" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
                <a href="#" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" aria-label="WhatsApp"><i class="fab fa-whatsapp"></i></a>
            </div>
            <p>&copy; 2023 Quebrada HOST. Todos os direitos reservados. Feito com orgulho na periferia.</p>
        </div>
    </footer>

    <script src="https://kit.fontawesome.com/SEU_CODIGO_FONT_AWESOME.js" crossorigin="anonymous"></script>
    </body>
</html>
