# Briefing — Site juliomartins.ai

> Especificação para implementação. Autor: Julio Martins + Jarvis. Data: 25/08/2026.
> O código entregue será hospedado no GitHub Pages e mantido MANUALMENTE (sem build) — leia as restrições técnicas antes de qualquer decisão.

## 1. O que é este site
Site pessoal-profissional de **Julio Martins**, posicionado na tese: **"Modernização de sistemas críticos sem ruptura operacional"**. Público-alvo: donos, CEOs e diretores de empresas cujos negócios dependem de sistemas legados. O site precisa transmitir **senioridade de engenharia e responsabilidade** — o oposto do visual "guru de IA" (nada de gradientes roxos, glassmorphism, emojis, robôs, cérebros digitais).

Tom: sóbrio, direto, confiante. Referência de vibe: sites de engenheiros sêniores e consultorias técnicas de respeito — tipografia forte, muito espaço em branco, números em destaque, zero enfeite gratuito.

## 2. Restrições técnicas (NÃO NEGOCIÁVEIS)
1. **HTML5 + CSS puro. Zero frameworks** (sem React, Vue, Tailwind, Bootstrap). JavaScript só se estritamente necessário, vanilla e mínimo.
2. **Zero build step.** Nada de npm, bundlers, geradores estáticos (sem Astro/Jekyll/Hugo). Os arquivos entregues são os arquivos servidos. Motivo: o site é mantido manualmente por commit — cada artigo novo é um HTML copiado de um template.
3. **Um único `styles.css` compartilhado** por todas as páginas. Design tokens (cores, tipografia, espaçamentos) como variáveis CSS no `:root`.
4. **Google Fonts permitido** (no máximo 2 famílias). Todo o resto self-contained.
5. **Responsivo mobile-first.** Sem scroll horizontal em nenhuma viewport.
6. **SEO básico em cada página:** `<title>` único, meta description, Open Graph (og:title, og:description, og:image), lang="pt-BR", HTML semântico (header/main/section/article/footer), heading hierarchy correta.
7. **Acessibilidade:** contraste AA, alt em toda imagem, foco visível.
8. **Performance:** sem bibliotecas, imagens otimizadas, página < 500KB.
9. Arquivo **`404.html`** incluído. **NÃO criar/alterar o arquivo `CNAME`** (já existe no repo).

## 3. Estrutura de arquivos (exatamente esta)
```
/index.html            ← home
/styles.css            ← único CSS do site
/404.html
/casos/index.html      ← lista de estudos de caso
/casos/br-captura.html ← 1º caso (usar conteúdo placeholder — ver §6)
/blog/index.html       ← lista de artigos
/blog/_template.html   ← MODELO de artigo (ver §7 — peça central do fluxo)
/assets/img/           ← imagens (usar placeholders)
```

## 4. Conteúdo da HOME (textos finais — usar exatamente estes)

**Header/nav:** logo "JULIO MARTINS" + links: Tese · Casos · Blog · Sobre · Contato.

**Hero:**
- H1: "Modernização de sistemas críticos **sem ruptura operacional**."
- Sub: "Eu lidero travessias: do sistema legado que sustenta o negócio para a plataforma que permite crescer — com a operação rodando o tempo inteiro."
- CTA primário: "Falar comigo" (→ #contato) · CTA secundário: "Ver a última travessia" (→ /casos/)

**Faixa de números (destaque visual forte):**
- **Zero** — downtime nos clientes de missão crítica durante toda a migração
- **4×** — crescimento da operação durante a travessia, não depois dela
- **100%** — do sistema legado desligado ao final
- **2,5 anos** — de migração do core, cliente a cliente, com escrita dupla até cada virada
- Nota pequena: "Números da última travessia liderada (2022–2026), em plataforma que gerencia milhões de simcards. Estudo de caso completo em publicação."

**Seção "A tese":**
- H2: "Modernizar não é reescrever código. É atravessar sem destruir valor."
- Parágrafo: "A IA tornou barato gerar código novo. O que continua raro é assumir a responsabilidade pela travessia: descobrir as regras de negócio que não estão documentadas, decidir o que preservar e o que substituir, operar o velho e o novo em paralelo, proteger receita e clientes — e desligar o legado só quando a equivalência está provada."
- 3 princípios (cards ou lista):
  1. **O problema é econômico, não técnico.** Stack antiga significa mão de obra cara e escassa, custo de recursos e risco crescente. A modernização certa ataca isso — não a moda tecnológica.
  2. **Primeiro estabilizar, depois migrar.** Ninguém faz travessia com o navio afundando. A primeira fase é parar a sangria e criar as condições — quem pula essa etapa migra o caos junto.
  3. **A operação nunca para.** Fundação, satélites, produto a produto, e o core cliente a cliente — com dados escritos dos dois lados até cada virada. Downtime não é acidente evitado; é resultado projetado.

**Seção "Sobre":**
- Texto: "Mais de 25 anos construindo e transformando sistemas que sustentam operações reais — atravessando gerações de tecnologia, de Clipper a IA. Perfil híbrido: arquitetura, produto, operação e negócio na mesma cadeira. Hoje aplico IA com método em modernização de sistemas críticos e na criação de ativos operacionais."
- `[PLACEHOLDER-IMG: foto profissional do Julio — assets/img/julio.jpg — usar imagem cinza com proporção 4:5 até a foto existir]`

**Seção "Contato":**
- H2: "Uma travessia à vista?"
- Texto: "Se a sua operação depende de um sistema que ficou velho — e parar não é opção — vale uma conversa."
- Botão LinkedIn: `[PLACEHOLDER-LINK: URL do LinkedIn do Julio]`
- `[PLACEHOLDER: e-mail profissional — decidir se será exibido]`

**Footer:** "© 2026 Julio Martins" + "juliomartins.ai".

## 5. Página /casos/index.html
Lista de estudos de caso em cards. Por enquanto **1 card**:
- Título: "Modernização com o avião voando" · Subtítulo: "Plataforma crítica migrada sem parar a operação — enquanto ela quadruplicava." · Estado: card clicável → /casos/br-captura.html
- Prever visualmente que a lista crescerá (2º e 3º cards podem aparecer como "Em publicação", desabilitados).

## 6. Página /casos/br-captura.html
Usar a estrutura abaixo com `[PLACEHOLDER]` — o texto final entra depois (aguarda autorização do cliente):
- Hero do caso: título + 1 parágrafo de resumo `[PLACEHOLDER-TEXTO: resumo executivo]`
- Tabela/grid "Antes → Depois" `[PLACEHOLDER-TABELA]`
- Seções: O ponto de partida · A decisão difícil · Estabilizar antes de migrar · O método (4 movimentos) · Resultados · Depoimento `[PLACEHOLDER-QUOTE: depoimento do CEO]`
- CTA final: "Falar comigo" → home#contato

## 7. Blog — A PEÇA CENTRAL DO FLUXO (leia com atenção)
O fluxo de publicação é: **copiar `/blog/_template.html` → preencher → adicionar 1 item em `/blog/index.html` → 1 commit**. Portanto:
- `_template.html` deve ser um arquivo de artigo COMPLETO e autoexplicativo, com comentários HTML indicando o que trocar: `<!-- TROCAR: título -->`, `<!-- TROCAR: data -->`, `<!-- TROCAR: descrição para SEO/OG -->`, e o corpo com exemplos de todos os elementos estilizados: h2, h3, parágrafo, lista, citação, tabela, imagem com legenda, bloco de código, destaque/callout.
- A tipografia do artigo é prioridade nº 1 do design: largura de leitura ~65ch, hierarquia clara, código legível.
- `/blog/index.html`: lista simples de artigos (título + data + resumo de 1 linha), mais recente no topo, com comentário HTML `<!-- NOVO ARTIGO: copie o <li> abaixo -->` marcando onde inserir.
- Sem paginação, sem tags, sem busca, sem RSS por enquanto — simplicidade primeiro.

## 8. Direção de design
- **Paleta sugerida** (pode refinar, mantendo a sobriedade): fundo off-white quente (#FAFAF7), texto grafite (#15181D), acento azul-aço (#0E5FA5), cinza para secundários. Uma cor de acento só.
- **Tipografia sugerida:** display geométrica forte para títulos (ex.: Archivo 800) + sans humanista para texto (ex.: Manrope). Máximo 2 famílias.
- Números da faixa de resultados são o elemento visual mais importante da home.
- Tema único (claro). Sem dark mode nesta versão.
- PROIBIDO: gradientes chamativos, animações decorativas, ícones de IA/robô, stock photos de tecnologia, carrosséis.

## 9. Critérios de aceite
- [ ] Estrutura de arquivos idêntica à do §3, sem arquivos extras de tooling
- [ ] Abre perfeito via file:// e no GitHub Pages sem nenhum build
- [ ] Um dev não-designer consegue publicar um artigo novo em 10 min só seguindo os comentários do _template
- [ ] Lighthouse: performance e acessibilidade > 90
- [ ] Todos os `[PLACEHOLDER]` claramente marcados e fáceis de localizar (buscar por "PLACEHOLDER")
