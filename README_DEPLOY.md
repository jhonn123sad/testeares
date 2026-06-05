# Método ARES Completo - pacote estático ARES

Este ZIP foi gerado pelo Admin do ARES e contém uma versão estática da área de membros.

## O que está preservado

- Curso, módulos, aulas e materiais cadastrados no Admin.
- Código de acesso salvo como hash SHA-256 no HTML.
- Progresso do aluno salvo no navegador com localStorage.
- Player de vídeo via YouTube embed.

## Arquivos principais

- `index.html`: aplicação completa.
- `404.html`: fallback para GitHub Pages.
- `_redirects`: fallback para Cloudflare Pages/Netlify.
- `_headers`: headers básicos de segurança.
- `.nojekyll`: evita processamento Jekyll no GitHub Pages.
- `wrangler.toml`: configuração simples para Cloudflare Pages.

## Cloudflare Pages pelo GitHub

1. Crie um repositório no GitHub.
2. Extraia este ZIP.
3. Envie todos os arquivos extraídos para a raiz do repositório.
4. No Cloudflare Pages, conecte esse repositório.
5. Use estas opções:
   - Framework preset: None
   - Build command: deixe vazio
   - Build output directory: /

## Cloudflare Pages por upload direto

Cloudflare Pages normalmente aceita upload de pasta, não ZIP comum.

1. Extraia este ZIP.
2. No Cloudflare Pages, use Upload assets/Direct Upload.
3. Selecione a pasta extraída inteira.

## GitHub Pages

1. Crie um repositório no GitHub.
2. Extraia este ZIP.
3. Envie todos os arquivos extraídos para a raiz do repositório.
4. Vá em Settings > Pages.
5. Em Build and deployment, selecione Deploy from a branch.
6. Escolha branch `main` e pasta `/root`.

As rotas usam hash, por exemplo `#/dashboard`, para funcionar também em subdiretórios como GitHub Pages.

## Wrangler opcional

Se usar Cloudflare Wrangler depois de extrair o ZIP:

```bash
npx wrangler pages deploy . --project-name ares
```

## Aviso importante

Este pacote é 100% estático. A senha funciona para bloquear a navegação no navegador, mas o hash fica dentro do HTML. Para conteúdo altamente sensível, use a versão Next.js com autenticação no servidor.
