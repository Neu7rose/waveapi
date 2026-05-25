# Wave API — Landing Page

Site oficial da **Wave API** — a API de músicas feita para servidores MTA:SA.

## 🚀 Como hospedar

### Vercel (recomendado)
1. Acesse [vercel.com](https://vercel.com) e crie uma conta
2. Clique em **"Add New Project"**
3. Faça upload da pasta ou conecte ao GitHub
4. O Vercel detecta automaticamente que é um site estático
5. Clique em **Deploy** — pronto em menos de 1 minuto

### Netlify
1. Acesse [netlify.com](https://netlify.com)
2. Arraste a pasta inteira para a área de drop da dashboard
3. Aguarde o deploy automático
4. Configure um domínio customizado em **Domain Settings**

### GitHub Pages
1. Crie um repositório no GitHub
2. Faça upload do `index.html` para a branch `main`
3. Vá em **Settings → Pages**
4. Em **Source**, selecione `Deploy from a branch` → `main` → `/ (root)`
5. Aguarde alguns minutos e acesse `https://seu-usuario.github.io/nome-do-repo`

### Hospedagem manual (qualquer servidor)
Qualquer servidor web que sirva arquivos estáticos funciona:
```bash
# Nginx - adicione ao seu server block:
location / {
    root /var/www/waveapi;
    index index.html;
}

# Apache - apenas coloque o index.html na pasta pública:
cp index.html /var/www/html/
```

## 📁 Estrutura dos arquivos

```
waveapi/
├── index.html    # Site completo (HTML + CSS + JS tudo em um arquivo)
├── README.md     # Este arquivo
└── api-docs.md   # Documentação da API em Markdown
```

## ⚙️ Customização

Todas as configurações estão no início do `<style>` no `index.html`:

```css
:root {
  --cyan: #00D4FF;        /* Cor primária */
  --cyan-bright: #00FFFF; /* Glow accent */
  --bg-deep: #080B10;     /* Background principal */
  --bg-card: #0D1117;     /* Background de cards */
}
```

Para alterar textos, preços ou conteúdo, basta editar o HTML diretamente — sem build step, sem dependências.

## 📝 Notas

- Zero dependências externas — funciona 100% offline após o carregamento
- Todos os ícones são SVG inline
- Fontes carregadas do Google Fonts (requer internet)
- Para uso completamente offline, substitua as fontes por fontes do sistema no CSS

## 📄 Licença

© 2025 Wave API — waveapi.fun
