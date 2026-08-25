# juliomartins.ai

Site pessoal-profissional de Julio Martins — tese: **modernização de sistemas críticos sem ruptura operacional**.

Hospedado no GitHub Pages, domínio `juliomartins.ai` (arquivo `CNAME`). **Sem build step**: os arquivos deste repositório são os arquivos servidos. HTML + CSS puros.

## Estado atual
- `index.html` — **v1 provisória** (feita pelo Jarvis), no ar até a versão final ser implementada a partir do `BRIEFING-MANUS.md`.
- `BRIEFING-MANUS.md` — especificação completa do site final (estrutura, conteúdo, restrições técnicas, critérios de aceite).

## Fluxo de publicação de artigo (1 artigo = 1 commit)
1. Copiar `blog/_template.html` → `blog/nome-do-artigo.html`
2. Preencher seguindo os comentários `<!-- TROCAR: ... -->`
3. Adicionar o item na lista de `blog/index.html`
4. Commit único: `post: <título do artigo>` → push → no ar

Convenções de commit:
- `post: <título>` — artigo novo
- `caso: <nome>` — estudo de caso novo ou atualizado
- `site: <mudança>` — ajustes de estrutura/design/conteúdo fixo

## DNS (registrador do domínio)
- 4 registros `A` em `@`: 185.199.108.153 · 185.199.109.153 · 185.199.110.153 · 185.199.111.153
- `CNAME` `www` → `julioemartins.github.io`
- Após propagação: ativar "Enforce HTTPS" nas configurações do Pages.
