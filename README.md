# Keyla Lourenço Saúde & Estética — site institucional

Página única em React 19 + Vite 6 + Tailwind CSS 4.

## Rodar localmente

```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # gera dist/
npm run lint     # checagem de tipos (tsc)
```

> **Windows corporativo:** se a política de grupo bloquear executáveis na pasta
> Downloads (erro "Permission denied" / "bloqueado por uma política de grupo"),
> mova o projeto para outra pasta (ex.: `C:\dev\keyla`) ou rode os comandos via
> `node node_modules/vite/bin/vite.js build` com a variável `ESBUILD_BINARY_PATH`
> apontando para uma cópia do `esbuild.exe` fora de Downloads.

## Onde editar o conteúdo

Tudo fica em [`src/data/clinicData.ts`](src/data/clinicData.ts):

- `CLINIC_INFO` — contato, endereço, horário, Instagram.
- `PHOTOS` — fotos reais da profissional e do consultório (hero, sobre, clínica).
  Enquanto estiverem `null`, o site usa composições com a identidade da marca.
- `PROCEDURE_CATEGORIES` — procedimentos (o campo `image` é opcional).
- `BEFORE_AFTER_CASES` e `TESTIMONIALS` — as seções "Resultados" e "Depoimentos"
  só aparecem quando essas listas têm itens reais e autorizados.

Fotos: salve em `src/assets/images/` em WebP ou JPG (lado maior com até ~1600 px),
importe no arquivo de dados e informe `width`/`height` reais.

## SEO

Antes de publicar, preencha em `index.html` o domínio definitivo
(`og:url`, `link rel="canonical"`, URL absoluta de `og:image`) e adicione um `sitemap.xml`.
