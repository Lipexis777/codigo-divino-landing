# Código Divino — Landing Page

Landing page de venda (uma página só, HTML/CSS puro, sem build) para o
e-book "Código Divino", com botão de compra apontando para o checkout
da Kiwify.

## Antes de divulgar: troque o link da Kiwify

No arquivo `index.html`, procure por `SUBSTITUIR-LINK-KIWIFY` (um único
lugar, no botão "Comprar ahora →") e troque pelo link real do checkout
do produto na Kiwify. Algo como:

```html
<a href="https://pay.kiwify.com.br/SEU-LINK-REAL" ...>
```

## Hospedagem gratuita (Vercel)

O site já foi publicado com `vercel deploy --temporary`, que não exige
login e gera uma URL pública na hora. Essa URL funciona, mas é
temporária/"não reivindicada" — fica live por um tempo, depois some se
ninguém assumir o projeto.

Para deixar fixo e de graça por tempo indeterminado (até valer a pena
comprar um domínio):

1. Crie uma conta grátis em https://vercel.com (pode usar login com
   GitHub).
2. No terminal, dentro desta pasta, rode:
   ```
   npx vercel login
   npx vercel link
   npx vercel --prod
   ```
3. Isso gera uma URL fixa tipo `codigo-divino-landing.vercel.app`,
   sem custo, enquanto você não tiver domínio próprio.

Também é possível reivindicar a *mesma* implantação temporária feita
agora: o `vercel deploy --temporary` imprime, junto com a URL, um link
de "claim" — abrindo esse link e logando você assume o projeto sem
perder o deploy já feito.

## Repositório no GitHub

O código também foi versionado e enviado para o GitHub (branch
`main`), então dá pra conectar esse repositório ao Vercel depois
(Import Project) para deploy automático a cada alteração.
