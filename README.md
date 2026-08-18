# ATHENA Conference 2027 — site publicado

Espelho de publicacao das landing pages da ATHENA 2027 Conference.
Servido por GitHub Pages em **https://conference.athenainternational.org/**

| URL | Arquivo |
|-----|---------|
| `/` | `index.html` (versao B, escolhida como principal) |
| `/a/` | `a/index.html` (versao A) |
| `/b/` | `b/index.html` (versao B) |
| `/thanks-athena/` | `thanks-athena/index.html` (pagina do hotel) |

## Nao editar os HTMLs aqui

Este repositorio e **gerado**. A fonte da verdade dos HTMLs fica no repo interno
`lua-sol-co`, em `Clients/athena-international/_aprovacao/2026-08-10_landing-pages-athena/`.
Edicao feita direto aqui e sobrescrita no proximo sync.

Pra publicar uma alteracao, rodar de dentro do repo `lua-sol-co`:

```bash
./Clients/athena-international/deploy-sync.sh          # copia + valida, sem commit
./Clients/athena-international/deploy-sync.sh --push   # copia + valida + commit + push
```

O script valida toda referencia local de imagem e CSS antes de deixar publicar.

## Imagens

Ficam em `assets/conference-2027/index-A-assets/` e `index-B-assets/` (uma copia por versao).
Sao WebP otimizados, servidos deste repo (nao usamos mais o Azure Blob).

Cards de speaker: **560x672**. Pra adicionar um:

```bash
cwebp -q 80 -m 6 -resize 560 0 origem.png \
  -o assets/conference-2027/index-A-assets/speakers/nome.webp
# repetir pra index-B-assets/
```

Os originais em resolucao cheia ficam no repo interno, em
`Clients/athena-international/assets/conference-2027-webp/`.
