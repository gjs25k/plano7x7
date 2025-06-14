# Instruções para Hospedagem no GitHub e Vercel

## Estrutura dos Arquivos

Você recebeu os seguintes arquivos para sua página de vendas:

1. `index.html` - Página principal de vendas
2. `hero-image.png` - Imagem principal da página
3. `README.md` - Este arquivo com instruções

## Como Hospedar no GitHub

### Passo 1: Criar um Repositório no GitHub

1. Acesse [GitHub.com](https://github.com) e faça login
2. Clique em "New repository" (Novo repositório)
3. Nomeie o repositório (ex: `alimentacao-leve-landing`)
4. Marque como "Public" (Público)
5. Marque "Add a README file"
6. Clique em "Create repository"

### Passo 2: Fazer Upload dos Arquivos

1. No seu repositório, clique em "uploading an existing file"
2. Arraste e solte os arquivos `index.html` e `hero-image.png`
3. Adicione uma mensagem de commit (ex: "Adicionar página de vendas")
4. Clique em "Commit changes"

### Passo 3: Ativar GitHub Pages

1. No seu repositório, vá em "Settings" (Configurações)
2. Role para baixo até "Pages" no menu lateral
3. Em "Source", selecione "Deploy from a branch"
4. Escolha "main" como branch
5. Clique em "Save"
6. Aguarde alguns minutos e sua página estará disponível em: `https://seuusuario.github.io/nome-do-repositorio`

## Como Hospedar no Vercel

### Opção 1: Conectar com GitHub (Recomendado)

1. Acesse [Vercel.com](https://vercel.com) e faça login
2. Clique em "New Project"
3. Conecte sua conta do GitHub
4. Selecione o repositório que você criou
5. Clique em "Deploy"
6. Aguarde o deploy e sua página estará disponível em um domínio Vercel

### Opção 2: Upload Direto

1. Acesse [Vercel.com](https://vercel.com) e faça login
2. Clique em "New Project"
3. Selecione "Browse All Templates"
4. Escolha "Static Site"
5. Faça upload dos arquivos `index.html` e `hero-image.png`
6. Clique em "Deploy"

## Personalizações Importantes

### 1. Adicionar Link de Compra

No arquivo `index.html`, procure pelos botões com `href="#"` e substitua pelos links reais da Kirvano ou Hotmart:

```html
<a href="SEU_LINK_DE_COMPRA_AQUI" class="cta-button">Quero Transformar Minha Alimentação!</a>
```

### 2. Inserir VSL (Vídeo Sales Letter)

Substitua o placeholder da VSL pelo código embed do seu vídeo:

```html
<div class="vsl-placeholder">
    <!-- Substitua por seu código de embed do vídeo -->
    <iframe src="SEU_VIDEO_AQUI" width="100%" height="400"></iframe>
</div>
```

### 3. Adicionar Pixel de Tracking

Adicione seus pixels do Facebook, Google Analytics, etc. antes do `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>

<!-- Facebook Pixel -->
<script>
  !function(f,b,e,v,n,t,s)
  {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
  n.callMethod.apply(n,arguments):n.queue.push(arguments)};
  if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
  n.queue=[];t=b.createElement(e);t.async=!0;
  t.src=v;s=b.getElementsByTagName(e)[0];
  s.parentNode.insertBefore(t,s)}(window, document,'script',
  'https://connect.facebook.net/en_US/fbevents.js');
  fbq('init', 'SEU_PIXEL_ID');
  fbq('track', 'PageView');
</script>
```

## Dicas de Otimização

1. **SEO**: A página já está otimizada com meta tags básicas
2. **Responsividade**: O design é responsivo para mobile e desktop
3. **Performance**: As imagens estão otimizadas
4. **Conversão**: Os CTAs estão estrategicamente posicionados

## Suporte

Se precisar de ajuda com a hospedagem ou personalização, consulte:
- [Documentação do GitHub Pages](https://docs.github.com/en/pages)
- [Documentação do Vercel](https://vercel.com/docs)

Sua página de vendas está pronta para converter! 🚀

