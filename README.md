# Escola-de-Instru-o-
Plantaforma Educativa com aulas, pesquisas,salas de aulas, livro,Ai , conexão com outras plataformas, WatsApp, FB, Instagram, turma, professores, alunos.
quadro virtual, inteligência artificial, uma área para ver os vídeos de diversas plataformas.




Criar <!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Escola de Instrução</title>
  <style>
    :root{
      --primary:#123b67;
      --secondary:#1d8a70;
      --bg:#f4f7fb;
      --white:#ffffff;
      --text:#172033;
      --muted:#667085;
      --border:#dce3ec;
      --danger:#c62828;
    }

    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      font-family:Arial, Helvetica, sans-serif;
      background:var(--bg);
      color:var(--text);
    }
    a{text-decoration:none;color:inherit}
    button,input,textarea,select{font:inherit}
    button{cursor:pointer}

    .topbar{
      background:var(--primary);
      color:white;
      padding:10px 5%;
      display:flex;
      justify-content:space-between;
      gap:10px;
      flex-wrap:wrap;
      font-size:14px;
    }

    .navbar{
      position:sticky;
      top:0;
      z-index:20;
      background:white;
      box-shadow:0 5px 20px rgba(0,0,0,.08);
    }

    .nav-inner{
      width:92%;
      max-width:1400px;
      margin:auto;
      padding:15px 0;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:15px;
      flex-wrap:wrap;
    }

    .brand{
      display:flex;
      align-items:center;
      gap:10px;
      color:var(--primary);
      font-weight:bold;
      font-size:18px;
    }

    .brand-icon{
      width:40px;height:40px;border-radius:12px;
      display:grid;place-items:center;
      background:var(--secondary);color:white;font-size:20px;
    }

    .nav-links{
      display:flex;
      gap:8px;
      flex-wrap:wrap;
    }

    .nav-links button{
      background:transparent;
      border:none;
      color:var(--text);
      padding:8px 10px;
      border-radius:8px;
      cursor:pointer;
    }

    .nav-links button.active{
      background:#e8f2ef;
      color:var(--secondary);
      font-weight:bold;
    }

    .menu-btn{
      display:none;
      background:var(--primary);
      color:white;
      border:none;
      border-radius:8px;
      padding:10px 14px;
      cursor:pointer;
    }

    .container{
      width:92%;
      max-width:1400px;
      margin:auto;
      padding-bottom:40px;
    }

    .page{
      display:none;
      padding:30px 0 50px;
    }

    .page.active{
      display:block;
      animation:appear .22s ease;
    }

    @keyframes appear{
      from{opacity:0;transform:translateY(8px)}
      to{opacity:1;transform:translateY(0)}
    }

    .hero{
      background:linear-gradient(135deg,var(--primary),var(--secondary));
      color:white;
      border-radius:20px;
      padding:50px 8%;
     58px);
    }

    .hero p{
      line-height:1.7;
      max-width:700px;
      margin-bottom:20px;
    }

    .section-title{
      margin:25px 0 15px;
      font-size:22px;
      color:var(--primary);
    }

    .grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:18px;
    }

    .card,.form-card{
      background:white;
      border:1px solid var(--border);
      border-radius:14px;
      padding:20px;
      box-shadow:0 5px 20px rgba(0,0,0,.08);
    }

    .card h3,.form-card h3{
      margin-top:0;
      color:var(--primary);
    }

    .card p{
      color:var(--muted);
      line-height:1.6;
    }

    .icon{
      font-size:34px;
      margin-bottom:10px;
    }

    .btn{
      display:inline-block;
      border:0;
      border-radius:8px;
      background:var(--secondary);
      color:white;
      padding:12px 18px;
      cursor:pointer;
      font-weight:bold;
      margin:5px 3px 0 0;
    }

    .btn.primary{
      background:white;
      color:var(--primary);
    }

    .btn.red{
      background:var(--danger);
    }

    .form-card{
      max-width:760px;
      margin:20px auto;
    }

    .form-group{
      margin-bottom:15px;
    }

    label{
      display:block;
      margin-bottom:6px;
      font-weight:bold;
    }

    input,textarea,select{
      width:100%;
      padding:12px;
      border:1px solid var(--border);
      border-radius:8px;
      background:white;
      color:var(--text);
    }

    textarea{
      min-height:120px;
      resize:vertical;
    }

    .notice{
      background:#eaf6ef;
      color:#185b42;
      border-radius:8px;
      padding:14px;
      margin:15px 0;
    }

    .notice.error{
      background:#ffeded;
      color:var(--danger);
    }

    .video-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:18px;
    }

    .video-card{
      background:white;
      border-radius:12px;
      overflow:hidden;
      box-shadow:0 5px 20px rgba(0,0,0,.08);
    }

    .video-card iframe{
      width:100%;
      aspect-ratio:16/9;
      border:0;
      display:block;
    }

    .video-content{
      padding:16px;
    }

    canvas{
      width:100%;
      height:auto;
      background:white;
      border:2px solid var(--border);
      border-radius:12px;
      display:block;
      touch-action:none;
    }

    .toolbar{
      display:flex;
      flex-wrap:wrap;
      gap:8px;
      margin-bottom:12px;
    }

    .toolbar button{
      border:1px solid var(--border);
      border-radius:8px;
      background:#edf3f8;
      color:var(--primary);
      padding:10px 12px;
      cursor:pointer;
    }

    footer{
      background:var(--primary);
      color:white;
      padding:35px 5%;
      margin-top:20px;
    }

    .footer-grid{
      width:92%;
      max-width:1400px;
      margin:auto;
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:20px;
    }

    .copyright{
      width:92%;
      max-width:1400px;
      margin:25px auto 0;
      padding-top:18px;
      text-align:center;
      border-top:1px solid rgba(255,255,255,.2);
    }

    #toast{
      position:fixed;
      right:18px;
      bottom:18px;
      z-index:60;
      display:none;
      background:#172033;
      color:white;
      padding:14px 18px;
      border-radius:10px;
      max-width:350px;
    }

    @media (max-width:860px){
      .menu-btn{display:block}
      .nav-links{
        display:none;
        width:100%;
        flex-direction:column;
      }
      .nav-links.open{display:flex}
      .nav-links button{width:100%;text-align:left}
    }
  </style>
</head>
<body>
  <div class="topbar">
    <span>🎓 Educação • Conhecimento • Desenvolvimento</span>
    <span>José Katuala João Menezes</span>
  </div>

  <header class="navbar">
    <div class="nav-inner">
      <div class="brand">
        <span class="brand-icon">🎓</span>
        <span>Escola de Instrução</span>
      </div>

      <button class="menu-btn" onclick="toggleMenu()">☰ Menu</button>

      <div id="navLinks" class="nav-links">
        <button class="active" onclick="showPage('inicio')">Início</button>
        <button onclick="showPage('professor')">Professor</button>
        <button onclick="showPage('estudante')">Estudante</button>
        <button onclick="showPage('salas')">Salas</button>
        <button onclick="showPage('biblioteca')">Biblioteca</button>
        <button onclick="showPage('pesquisa')">Pesquisa</button>
        <button onclick="showPage('estudio')">Estúdio</button>
        <button onclick="showPage('livros')">Livros</button>
        <button onclick="showPage('quadro')">Quadro</button>
        <button onclick="showPage('ia')">IA</button>
        <button onclick="showPage('redes')">Redes</button>
        <button onclick="showPage('acesso')">Acesso</button>
      </div>
    </div>
  </header>

  <main class="container">
    <section id="inicio" class="page active">
      <div class="hero">
        <h1>Aprender. Ensinar. Evoluir.</h1>
        <p>Plataforma educativa para professores, instrutores, estudantes e comunidade escolar com aulas, pesquisa, salas, livros, IA, estúdio e redes sociais.</p>
        <button class="btn primary" onclick="showPage('estudante')">Área do estudante</button>
        <button class="btn" onclick="showPage('professor')">Publicar aula</button>
      </div>

      <div class="section-title">Áreas da plataforma</div>

      <div class="grid">
        <article class="card">
          <div class="icon">👨‍🏫</div>
          <h3>Professor</h3>
          <p>Publicar aulas e gerir materiais.</p>
          <button class="btn" onclick="showPage('professor')">Abrir</button>
        </article>

        <article class="card">
          <div class="icon">🎓</div>
          <h3>Estudante</h3>
          <p>Acompanhar aulas e tarefas.</p>
          <button class="btn" onclick="showPage('estudante')">Abrir</button>
        </article>

        <article class="card">
          <div class="icon">🔎</div>
          <h3>Pesquisa</h3>
          <p>Pesquisar qualquer assunto e vídeos.</p>
          <button class="btn" onclick="showPage('pesquisa')">Abrir</button>
        </article>

        <article class="card">
          <div class="icon">🤖</div>
          <h3>IA</h3>
          <p>Gerar explicações e materiais.</p>
          <button class="btn" onclick="showPage('ia')">Abrir</button>
        </article>
      </div>
    </section>

    <section id="professor" class="page">
      <div class="section-title">Área do professor</div>

      <div class="form-card">
        <h3>Publicar uma aula</h3>
        <form id="lessonForm">
          <div class="form-group">
            <label for="lessonTitle">Título da aula</label>
            <input id="lessonTitle" required />
          </div>

          <div class="form-group">
            <label for="lessonSubject">Disciplina</label>
            <input id="lessonSubject" required />
          </div>

          <div class="form-group">
            <label for="lessonDescription">Descrição</label>
            <textarea id="lessonDescription" required></textarea>
          </div>

          <div class="form-group">
            <label for="lessonVideo">URL do vídeo</label>
            <input id="lessonVideo" type="url" />
          </div>

          <button type="submit" class="btn">Guardar aula</button>
        </form>
      </div>

      <div class="section-title">Aulas publicadas</div>
      <div id="lessonsList" class="grid"></div>
    </section>

    <section id="estudante" class="page">
      <div class="section-title">Área do estudante</div>
      <div class="grid">
        <article class="card">
          <div class="icon">📚</div>
          <h3>Minhas aulas</h3>
          <p>Consultar materiais e aulas.</p>
          <button class="btn" onclick="showPage('professor')">Abrir</button>
        </article>

        <article class="card">
          <div class="icon">📝</div>
          <h3>Atividades</h3>
          <p>Registar tarefas e estudos.</p>
          <button class="btn" onclick="showToast('Área de atividades')">Abrir</button>
        </article>

        <article class="card">
          <div class="icon">📖</div>
          <h3>Biblioteca</h3>
          <p>Ler conteúdos digitais.</p>
          <button class="btn" onclick="showPage('biblioteca')">Abrir</button>
        </article>
      </div>
    </section>

    <section id="salas" class="page">
      <div class="section-title">Salas de aulas</div>
      <div class="grid">
        <article class="card">
          <div class="icon">🏫</div>
          <h3>Sala de Matemática</h3>
          <p>Exercícios e explicações.</p>
          <button class="btn" onclick="enterRoom('Matemática')">Entrar</button>
        </article>

        <article class="card">
          <div class="icon">🌍</div>
          <h3>Sala de Línguas</h3>
          <p>Aprender comunicação.</p>
          <button class="btn" onclick="enterRoom('Línguas')">Entrar</button>
        </article>

        <article class="card">
          <div class="icon">💻</div>
          <h3>Sala de Informática</h3>
          <p>Programação e tecnologia.</p>
          <button class="btn" onclick="enterRoom('Informática')">Entrar</button>
        </article>
      </div>

      <div id="roomInfo" class="notice" style="display:none;"></div>
    </section>

    <section id="biblioteca" class="page">
      <div class="section-title">Biblioteca digital</div>

      <div class="form-card">
        <h3>Adicionar material</h3>
        <form id="libraryForm">
          <div class="form-group">
            <label for="libraryTitle">Título</label>
            <input id="libraryTitle" required />
          </div>

          <div class="form-group">
            <label for="libraryCategory">Categoria</label>
            <select id="libraryCategory">
              <option>Livro</option>
              <option>Artigo</option>
              <option>Documento</option>
              <option>Material</option>
            </select>
          </div>

          <div class="form-group">
            <label for="libraryUrl">Link</label>
            <input id="libraryUrl" type="url" required />
          </div>

          <button type="submit" class="btn">Guardar material</button>
        </form>
      </div>

      <div id="libraryList" class="grid"></div>
    </section>

    <section id="pesquisa" class="page">
      <div class="section-title">Pesquisa geral</div>

      <div class="form-card">
        <h3>Pesquisar qualquer assunto</h3>
        <form id="searchForm">
          <div class="form-group">
            <label for="searchInput">Tema</label>
            <input id="searchInput" type="search" placeholder="Ex.: matemática, saúde..." required />
          </div>

          <div class="form-group">
            <label for="searchType">Tipo</label>
            <select id="searchType">
              <option value="all">Tudo</option>
              <option value="web">Web</option>
              <option value="videos">Vídeos</option>
            </select>
          </div>

          <button type="submit" class="btn">🔎 Pesquisar</button>
        </form>
      </div>

      <div id="searchStatus" class="notice" style="display:none;"></div>
      <div class="section-title">Resultados da web</div>
      <div id="webResults" class="grid"></div>

      <div class="section-title">Vídeos do YouTube</div>
      <div id="youtubeResults" class="video-grid"></div>
    </section>

    <section id="estudio" class="page">
      <div class="section-title">Estúdio de vídeos</div>

      <div class="form-card">
        <h3>Adicionar vídeo</h3>
        <form id="videoForm">
          <div class="form-group">
            <label for="videoTitle">Título</label>
            <input id="videoTitle" required />
          </div>

          <div class="form-group">
            <label for="videoFile">Ficheiro</label>
            <input id="videoFile" type="file" accept="video/*" />
          </div>

          <button type="submit" class="btn">Adicionar ao estúdio</button>
        </form>
      </div>

      <div id="videoList" class="grid"></div>
    </section>

    <section id="livros" class="page">
      <div class="section-title">Editor de livros</div>

      <div class="form-card">
        <h3>Criar livro</h3>
        <form id="bookForm">
          <div class="form-group">
            <label for="bookTitle">Título</label>
            <input id="bookTitle" required />
          </div>

          <div class="form-group">
            <label for="bookContent">Conteúdo</label>
            <textarea id="bookContent" required></textarea>
          </div>

          <button type="submit" class="btn">Guardar livro</button>
        </form>
      </div>

      <div id="bookList" class="grid"></div>
    </section>

    <section id="quadro" class="page">
      <div class="section-title">Quadro virtual</div>

      <div class="card">
        <div class="toolbar">
          <button onclick="setTool('pen')">✏️ Pincel</button>
          <button onclick="setTool('eraser')">🧽 Borracha</button>
          <button onclick="clearBoard()">🗑️ Limpar</button>
          <button onclick="saveBoard()">💾 Guardar</button>
        </div>

        <canvas id="board" width="1200" height="500"></canvas>
      </div>
    </section>

    <section id="ia" class="page">
      <div class="section-title">Inteligência artificial educativa</div>

      <div class="form-card">
        <h3>Pergunte à IA</h3>
        <form id="aiForm">
          <div class="form-group">
            <label for="aiQuestion">Pergunta</label>
            <textarea id="aiQuestion" placeholder="Ex.: Crie uma aula sobre frações." required></textarea>
          </div>

          <button type="submit" class="btn">Perguntar</button>
        </form>

        <div id="aiResult" class="notice">A resposta da IA aparecerá aqui.</div>
      </div>
    </section>

    <section id="redes" class="page">
      <div class="section-title">Redes sociais</div>

      <div class="grid">
        <article class="card">
          <div class="icon">💬</div>
          <h3>WhatsApp</h3>
          <p>Partilhar a plataforma.</p>
          <button class="btn" onclick="shareWhatsApp()">Partilhar</button>
        </article>

        <article class="card">
          <div class="icon">📘</div>
          <h3>Facebook</h3>
          <p>Partilhar no Facebook.</p>
          <button class="btn" onclick="shareFacebook()">Partilhar</button>
        </article>

        <article class="card">
          <div class="icon">📸</div>
          <h3>Instagram</h3>
          <p>Aceder ao Instagram.</p>
          <a href="https://www.instagram.com/" target="_blank" class="btn">Abrir Instagram</a>
        </article>
      </div>
    </section>

    <section id="acesso" class="page">
      <div class="section-title">Acesso à plataforma</div>

      <div id="userInfo" class="notice" style="display:none;"></div>

      <div class="grid">
        <div class="form-card">
          <h3>Criar conta</h3>
          <form id="registerForm">
            <div class="form-group">
              <label for="registerName">Nome completo</label>
              <input id="registerName" required />
            </div>

            <div class="form-group">
              <label for="registerEmail">Email</label>
              <input id="registerEmail" type="email" required />
            </div>

            <div class="form-group">
              <label for="registerPassword">Senha</label>
              <input id="registerPassword" type="password" required />
            </div>

            <div class="form-group">
              <label for="registerType">Tipo</label>
              <select id="registerType">
                <option value="estudante">Estudante</option>
                <option value="professor">Professor</option>
                <option value="instrutor">Instrutor</option>
              </select>
            </div>

            <button type="submit" class="btn">Criar conta</button>
          </form>
        </div>

        <div class="form-card">
          <h3>Entrar</h3>
          <form id="loginForm">
            <div class="form-group">
              <label for="loginEmail">Email</label>
              <input id="loginEmail" type="email" required />
            </div>

            <div class="form-group">
              <label for="loginPassword">Senha</label>
              <input id="loginPassword" type="password" required />
            </div>

            <button type="submit" class="btn">Entrar</button>
          </form>

          <button id="logoutBtn" class="btn red" style="display:none;">Terminar sessão</button>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="footer-grid">
      <div>
        <h3>Escola de Instrução</h3>
        <p>Plataforma para aprender, ensinar e evoluir.</p>
      </div>

      <div>
        <h3>Recursos</h3>
        <p>Aulas, vídeos, salas, livros, IA e pesquisa.</p>
      </div>

      <div>
        <h3>Proprietário</h3>
        <p>José Katuala João Menezes</p>
      </div>
    </div>

    <div class="copyright">© 2026 Escola de Instrução de Diversas Disciplinas</div>
  </footer>

  <div id="toast"></div>

  