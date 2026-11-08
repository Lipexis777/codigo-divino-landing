# Código Divino — Landing Page

Landing page de venda (uma página só, HTML/CSS puro, sem build) para o
e-book "Código Divino", com botão de compra apontando para o checkout
da Kiwify.

## 🌐 Site no ar agora (grátis)

https://lipexis777.github.io/codigo-divino-landing/

Publicado via GitHub Pages a partir deste repositório (branch `main`).
Não expira e não tem custo — serve bem até valer a pena comprar um
domínio próprio.

## ⚠️ Antes de divulgar: troque o link da Kiwify

No arquivo `index.html`, procure por `SUBSTITUIR-LINK-KIWIFY` (único
lugar, no botão "Comprar ahora →") e troque pelo link real do checkout
do produto na Kiwify, algo como:

```html
<a href="https://pay.kiwify.com.br/SEU-LINK-REAL" ...>
```

Depois de editar, suba a alteração (veja "Como atualizar o site"
abaixo) — o GitHub Pages atualiza sozinho em cerca de 1 minuto.

## Como atualizar o site

Se o `git push` normal funcionar no seu computador, é só:
```
git add index.html
git commit -m "fix: link da kiwify"
git push
```

Se preferir, também dá pra editar o arquivo direto pela interface do
GitHub (https://github.com/Lipexis777/codigo-divino-landing) — clique
em `index.html` → ícone de lápis → editar → "Commit changes".

## Quando valer a pena investir num domínio

Duas opções simples, ambas sem precisar recriar o site:

1. **Domínio apontando pro GitHub Pages** (mais barato/direto): compre
   o domínio em qualquer registrador, crie um arquivo `CNAME` na raiz
   do repo com o domínio, e configure o DNS conforme a documentação do
   GitHub Pages.
2. **Migrar para Vercel com domínio próprio**: crie uma conta grátis em
   https://vercel.com, rode `npx vercel link` e `npx vercel --prod`
   dentro desta pasta, e depois adicione o domínio no painel do
   projeto.

## Deploy alternativo já feito na Vercel (temporário)

Também foi gerado um deploy anônimo na Vercel, sem precisar de login:
isso cria uma URL pública na hora, mas que **expira em 1 hora** se
ninguém "reivindicar" (claim). Não é a opção recomendada para manter
no ar — o GitHub Pages acima é a opção permanente e gratuita.
