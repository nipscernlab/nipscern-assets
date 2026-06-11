# nipscern-assets

Acervo de mídia do site [nipscern.com](https://nipscern.com), servido via GitHub Pages
atrás do cache do Cloudflare no endereço **https://cdn.nipscern.com**.

Este repositório existe para manter o repositório do site
([nipscernlab/nipscernweb](https://github.com/nipscernlab/nipscernweb)) leve:
aqui ficam apenas os arquivos pesados (PDFs de publicações, vídeos, imagens
grandes, dados do CGVWeb). O código e as imagens leves de interface continuam
no repositório do site.

## Estrutura

| Pasta | Conteúdo | URL pública |
|---|---|---|
| `publications/` | PDFs de teses, dissertações e artigos (otimizados) | `cdn.nipscern.com/publications/...` |
| `videos/` | Vídeos re-encodados (1080p, H.264) | `cdn.nipscern.com/videos/...` |
| `images/` | Imagens grandes (WebP, largura máx. 2560 px) | `cdn.nipscern.com/images/...` |
| `cgvweb/` | Geometria e arquivos de evento do CGVWeb | `cdn.nipscern.com/cgvweb/...` |
| `archives/` | Pacotes (tours 360°, panorâmicas) | `cdn.nipscern.com/archives/...` |

## Regras de contribuição

1. **Arquivos são imutáveis.** O CDN guarda cache por 1 ano, então nunca
   substitua um arquivo existente: adicione uma versão com nome novo.
2. **Otimize antes de subir.** PDFs passam por Ghostscript, vídeos são
   re-encodados para 1080p, imagens viram WebP. O guia está em
   `docs/migration/` no repositório do site.
3. **Limite de 95 MB por arquivo** (o GitHub bloqueia 100 MB; o CI deste
   repositório recusa qualquer arquivo acima de 95 MB).
4. **Nomes em kebab-case**, sem espaços e sem acentos:
   `mest-2025-lucca-oliveira.pdf`, não `MEST 2025 Lucca Oliveira.pdf`.

## Acesso e licença

Repositório mantido pelo NIPSCERN (UFJF). Membros da organização têm acesso
de escrita; contribuições externas são bem-vindas via pull request.

O acervo é regido pela [Licença NIPSCERN 1.0](LICENSE.md). Atenção: PDFs de
teses e dissertações pertencem aos seus autores, e a mídia do CERN segue os
termos do CERN, conforme os créditos do site.
