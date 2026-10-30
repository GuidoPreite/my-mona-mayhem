<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematização orientada ao design

---

Nesta parte, você vai usar os fluxos de planejamento e implementação do Copilot para projetar uma transformação completa do tema. Esse é um processo de desenvolvimento orientado ao design: comece com uma visão, itere nos elementos visuais e deixe o Copilot cuidar do trabalho pesado de CSS.

## Tarefa 1: Planeje o tema retrô

<!-- track:vscode:start -->
Mude para o modo **Plan** no GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Use `/plan` no GitHub Copilot CLI ou pressione **Shift+Tab** até ativar o modo de planejamento.
<!-- track:cli:end -->

Insira este prompt:

> Quero transformar esta página em uma experiência completa de fliperama retrô. Planeje uma reformulação visual abrangente que inclua: efeitos de linhas de varredura CRT no fundo, brilho neon pulsante no título, selo VS animado com mudanças nas cores do gradiente, sobreposição de brilho e reflexos nos cartões de resultados, animações de entrada flutuante nos campos, texto de carregamento que muda entre verde e roxo e efeitos de brilho ao passar o cursor sobre os quadrados de contribuição. Mantenha o fundo escuro (`#0a0a1a`) com detalhes em verde (`#5fed83`) e roxo (`#8a2be2`). Use um tema escuro com a fonte retrô Press Start 2P do Google Fonts.

O Copilot vai gerar um plano detalhado com todos os efeitos visuais. **Não aceite imediatamente** — revise o plano e itere:

- Sugira ajustes no ritmo das animações (por exemplo, *"Deixe a pulsação neon mais lenta, em torno de 3 segundos"*).
- Pergunte sobre efeitos específicos (por exemplo, *"Como a sobreposição de reflexos funcionará nos cartões?"*).
- Peça mudanças na abordagem se algo não parecer adequado.

## Tarefa 2: Implemente o tema

Quando estiver satisfeito com o plano, peça ao Copilot para implementá-lo.

> Implemente o plano do tema de fliperama retrô que acabamos de criar.

O Copilot vai adicionar várias animações CSS, pseudoelementos e transições na folha de estilos. Por exemplo:

- `@keyframes` para scanlines, pulsação neon, shimmer e animações de entrada flutuante.
- Pseudoelementos (`::before`, `::after`) para efeitos de sobreposição.
- Propriedades personalizadas de CSS para as cores do tema.
- Transições e estados de hover para elementos interativos.

<!-- track:cli:start -->
Depois que as alterações forem aplicadas, use `/diff` para revisá-las antes de aprovar.
<!-- track:cli:end -->

## Tarefa 3: Ajuste o visual

> **⚠️ Não está vendo as alterações?** Se o novo tema ou as animações não aparecerem, pare o servidor (`Ctrl+C`), reinicie com `npm run dev` e atualize o navegador completamente com **Ctrl+Shift+R**.

Mantenha a prévia do navegador aberta e itere no design. Experimente prompts como:

> O efeito das linhas de varredura está forte demais; reduza a opacidade para 0.03.

> Adicione uma cintilação elétrica sutil ao texto do título.

> O selo VS deveria pulsar com mais intensidade.

Esse é um processo de **desenvolvimento orientado ao design**: você itera na saída visual em tempo real. Cada prompt refina a experiência. Não se contente com algo apenas «bom o suficiente» — continue aprimorando o visual até a página parecer pertencer a um fliperama.

## Tarefa 4: Atualize as instruções

Suas instruções devem refletir as decisões importantes de design para manter os prompts seguintes alinhados.

<!-- track:vscode:start -->
Peça ao Copilot Chat:

> Add a design guide section to copilot-instructions.md describing our retro arcade theme: colors, fonts, animation style
<!-- track:vscode:end -->

<!-- track:cli:start -->
Peça ao Copilot CLI:

> Update our repository instructions with a short design guide for the retro arcade theme: colors, fonts, animation style, and the rule that new UI should keep the neon aesthetic.
<!-- track:cli:end -->

Faça commit das instruções e das alterações de design quando a página estiver como você quer.

## ✅ Parte 4 concluída

**O que você aprendeu:**

- Usar fluxos de planejamento para projetar um **sistema visual antes de implementá-lo**.
- **Iterar na saída visual** usando prompts de acompanhamento.
- **Atualizar as instruções após decisões importantes** para manter a identidade visual.
