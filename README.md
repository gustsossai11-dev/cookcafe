# COOK CAFE — Landing Page (pacote para GitHub + Vercel)

Pacote **multi-arquivo**, pronto para versionar no GitHub e publicar na Vercel.
As imagens são arquivos separados na pasta `assets/` (sem base64), então nenhum
arquivo é grande demais para o GitHub.

## Estrutura
```
├── index.html        → a página
├── support.js        → runtime da página
├── image-slot.js     → componente auxiliar
└── assets/           → todas as imagens (logo, cookies, cafés, brownies)
```

## Publicar na Vercel
1. Suba esta pasta para um repositório no GitHub.
2. Na Vercel: **Add New → Project → Import** o repositório.
3. Framework Preset: **Other**. Sem build. Output: a própria raiz.
4. Deploy. Pronto — a Vercel serve o `index.html` automaticamente.

> Alternativa sem GitHub: em vercel.com → Add New → Project, arraste esta pasta.

## Rodar localmente
Precisa de um servidor estático simples (por causa dos arquivos externos):
```
npx serve .
```
ou a extensão **Live Server** do VSCode. Abrir o `index.html` com duplo clique
direto do disco pode bloquear o carregamento dos `.js` em alguns navegadores;
com o servidor local funciona sempre.

## Observação técnica
O `index.html` carrega React da internet (CDN unpkg) na primeira vez. Em
hospedagem online (Vercel/GitHub Pages) isso é automático. Por isso este pacote
é ideal para publicar, e o arquivo único offline é melhor só para envio avulso.

## Ainda a preencher antes de publicar
Preços (R$ XX,XX), endereço/horário/telefone, ponto do mapa, depoimentos reais,
links reais dos botões (iFood/WhatsApp/cardápio) e remover o aviso de demonstração.
