# Cantina do Campus - Exercício do Encontro 4

Projeto ajustado para corrigir os erros de CSS propostos em aula e estruturar a página usando Flexbox, seguindo o layout de referência.

## O que foi corrigido no `style.css`

1. **Cascata:** O `h1` tinha um `!important` desnecessário forçando a cor do título. Removi a declaração para respeitar o fluxo natural do CSS.
2. **Especificidade:** A classe `.promocao` não deixava o preço vermelho porque o seletor `#cardapio .preco` usava ID e tinha mais força. Ajustei para `#cardapio .preco.promocao` para garantir a prioridade.
3. **Box Model:** Os cartões estavam a estourar a largura da tela e a criar barra de rolagem horizontal. Adicionei `box-sizing: border-box` no reset global para incluir o padding e as bordas no tamanho final do elemento.
4. **Contraste:** O subtítulo estava com uma cor muito clara (`#c4c4c4`), dificultando a leitura no fundo branco. Mudei para `#595959` para atingir um contraste confortável (acima de 4,5:1).
5. **Foco:** O estilo de foco do menu estava com `outline: none`, o que deixava a navegação por teclado (tecla Tab) invisível. Tirei essa regra e adicionei um contorno visível nos links.
6. **Alinhamento:** O menu foi empurrado para a direita com um `margin-left: 610px` fixo. Removi essa margem manual e fiz o alinhamento correto usando Flexbox no topo.

## Layout com Flexbox

- **Topo (`.topo`):** Usei `display: flex` com `justify-content: space-between` para encostar a marca na esquerda e os links do menu na direita.
- **Menu (`.menu ul`):** Coloquei `display: flex` e `gap: 20px` para alinhar os links lado a lado de forma simples.
- **Cartões (`.cartoes`):** Apliquei `display: flex` com `flex-wrap: wrap` no container e `flex: 1 1 250px` nos cartões. Assim, eles ficam divididos lado a lado em telas grandes e adaptam-se para baixo se a janela for mais estreita.
