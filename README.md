# 🚀 Portfólio Miguel Caldas - FrontEnd & UI/UX Designer

Portfólio pessoal moderno e responsivo desenvolvido com HTML5, CSS3 e JavaScript puro.

## ✨ Características

- **Design Moderno e Minimalista** - Interface limpa e profissional
- **Totalmente Responsivo** - Adaptado para todos os dispositivos (desktop, tablet, mobile)
- **Animações Suaves** - Transições e efeitos que melhoram a experiência do usuário
- **Navegação Intuitiva** - Menu fixo com indicador de seção ativa
- **Seções Completas**:
  - Hero/Home com apresentação
  - Sobre com informações pessoais
  - Skills com barras de progresso animadas
  - Educação com timeline
  - Projetos em grid responsivo
  - Formulário de contato funcional
- **Efeitos Interativos**:
  - Scroll reveal animations
  - Hover effects nos cards
  - Parallax no hero
  - Typing effect no título
  - Custom cursor (desktop)
  - Botão back to top

## 📁 Estrutura de Arquivos

```
portfolio/
│
├── index.html      # Estrutura principal do site
├── style.css       # Estilos e design
├── script.js       # Interatividade e animações
└── README.md       # Este arquivo
```

## 🎨 Como Personalizar

### 1. **Informações Pessoais**

No arquivo `index.html`, edite:

```html
<!-- Linha ~30: Nome e descrição -->
<h1 class="hero-title">Seu Nome Aqui</h1>
<h2 class="hero-subtitle">Sua Profissão</h2>

<!-- Linha ~100: Informações sobre você -->
<p>Sua descrição pessoal...</p>

<!-- Linha ~150: Email, telefone, etc -->
<a href="mailto:seu-email@exemplo.com">seu-email@exemplo.com</a>
```

### 2. **Links de Redes Sociais**

Atualize seus links (presentes em 3 locais):

```html
<!-- Hero section -->
<a href="SEU_LINKEDIN" target="_blank">
<a href="SEU_GITHUB" target="_blank">
<a href="SEU_DRIBBBLE" target="_blank">
<a href="SEU_BEHANCE" target="_blank">
```

### 3. **Skills e Percentagens**

No arquivo `index.html`, seção Skills (~linha 200):

```html
<div class="skill-item">
    <div class="skill-header">
        <span>Nome da Skill</span>
        <span>85%</span> <!-- Ajuste a percentagem -->
    </div>
    <div class="skill-bar">
        <div class="skill-progress" style="width: 85%"></div> <!-- Mesma % -->
    </div>
</div>
```

### 4. **Educação/Formação**

Edite a timeline de educação (~linha 280):

```html
<div class="timeline-item">
    <div class="timeline-content">
        <span class="timeline-date">2023 - Presente</span>
        <h3>Nome do Curso</h3>
        <p class="timeline-institution">Nome da Instituição</p>
        <p>Descrição do curso...</p>
    </div>
</div>
```

### 5. **Projetos**

Substitua as imagens placeholder e informações (~linha 310):

```html
<div class="project-card">
    <div class="project-image">
        <img src="caminho/para/sua/imagem.jpg" alt="Projeto">
        <div class="project-overlay">
            <a href="URL_DO_PROJETO" class="project-link" target="_blank">
                <i class="fas fa-external-link-alt"></i>
            </a>
        </div>
    </div>
    <div class="project-info">
        <h3>Nome do Projeto</h3>
        <p>Descrição breve...</p>
        <div class="project-tags">
            <span>React</span>
            <span>CSS</span>
        </div>
    </div>
</div>
```

### 6. **Adicionar sua Foto**

Substitua o placeholder na seção Hero (~linha 50):

```html
<div class="hero-image">
    <!-- Remova o placeholder e adicione: -->
    <img src="caminho/para/sua/foto.jpg" alt="Miguel Caldas" 
         style="width: 400px; height: 400px; border-radius: 50%; 
                object-fit: cover; box-shadow: 0 20px 40px rgba(0, 0, 0, 0.2);">
</div>
```

### 7. **Cores do Tema**

No arquivo `style.css` (~linha 12), personalize as cores:

```css
:root {
    --primary-color: #667eea;    /* Cor principal */
    --secondary-color: #764ba2;  /* Cor secundária */
    --accent-color: #f093fb;     /* Cor de destaque */
    /* ... outras cores ... */
}
```

### 8. **Formulário de Contato**

Para fazer o formulário funcionar com backend real:

**Opção 1: EmailJS (Grátis)**
```javascript
// No script.js, substitua a função do formulário:
emailjs.send("service_id", "template_id", formData)
    .then(() => showNotification('Enviado!', 'success'));
```

**Opção 2: Formspree (Grátis)**
```html
<!-- No index.html, adicione action ao form: -->
<form action="https://formspree.io/f/SEU_ID" method="POST">
```

**Opção 3: Seu próprio backend**
```javascript
fetch('/api/contact', {
    method: 'POST',
    body: JSON.stringify(formData)
})
```

## 🚀 Como Usar

### Uso Local

1. **Clone ou baixe os arquivos**
2. **Abra o `index.html` em seu navegador**
3. Pronto! O site estará funcionando localmente

### Deploy/Hospedagem

**Opções gratuitas recomendadas:**

1. **GitHub Pages** (Recomendado)
   - Crie um repositório no GitHub
   - Faça upload dos arquivos
   - Vá em Settings > Pages
   - Selecione a branch main
   - Seu site estará em: `seuusuario.github.io/portfolio`

2. **Netlify**
   - Arraste a pasta para netlify.com/drop
   - Deploy instantâneo!

3. **Vercel**
   - Conecte seu repositório GitHub
   - Deploy automático

4. **Cloudflare Pages**
   - Upload via Git ou dashboard
   - CDN global gratuito

## 📝 Customizações Avançadas

### Adicionar Tema Escuro

```javascript
// Adicione ao script.js:
const themeToggle = document.createElement('button');
themeToggle.innerHTML = '<i class="fas fa-moon"></i>';
// Implementar lógica de toggle...
```

### Google Analytics

```html
<!-- Adicione antes do </head>: -->
<script async src="https://www.googletagmanager.com/gtag/js?id=SEU_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'SEU_ID');
</script>
```

### SEO

```html
<!-- Adicione no <head>: -->
<meta property="og:title" content="Miguel Caldas - Portfolio">
<meta property="og:description" content="FrontEnd Developer & UI/UX Designer">
<meta property="og:image" content="URL_DA_SUA_IMAGEM">
<meta property="og:url" content="URL_DO_SEU_SITE">
<meta name="twitter:card" content="summary_large_image">
```

## 🛠 Tecnologias Utilizadas

- **HTML5** - Estrutura semântica
- **CSS3** - Estilização moderna (Flexbox, Grid, Animations)
- **JavaScript (ES6+)** - Interatividade
- **Font Awesome 6** - Ícones
- **Google Fonts** - Tipografia (Inter)

## 📱 Compatibilidade

- ✅ Chrome (recomendado)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Opera
- ✅ Mobile browsers

## 💡 Dicas

1. **Otimize as imagens** - Use formatos WebP ou comprima JPG/PNG
2. **Adicione alt text** - Melhora acessibilidade e SEO
3. **Teste em diferentes dispositivos** - Use DevTools do navegador
4. **Mantenha atualizado** - Adicione novos projetos regularmente
5. **Use suas cores** - Personalize o tema para sua identidade visual
6. **Peça feedback** - Compartilhe com amigos e colegas

## 📞 Suporte

Se tiver dúvidas ou precisar de ajuda:

- 📧 Email: miguel.caldas@example.com
- 💼 LinkedIn: [Miguel Caldas](https://www.linkedin.com/in/miguel-caldas-7275a8212/)

## 📄 Licença

Este projeto está livre para uso pessoal. Sinta-se à vontade para modificar e usar como preferir!

---

**Desenvolvido com ❤️ por Miguel Caldas**

*Última atualização: Janeiro 2024*
