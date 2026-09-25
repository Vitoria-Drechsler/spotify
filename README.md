# Clone da Tela de Login do Spotify

Trabalho G1 da disciplina de **Front-End** — Universidade Atitus
Professor: Matheus Henrique Barquette
Construção de página web com HTML e CSS.

## Dupla
| Caroline Russo Zilio | 1140047 |
| Vitória Drechsler | 1139410 |

## Página de referência

Tela de login do Spotify: <https://accounts.spotify.com/pt-BR/login>


O objetivo foi reproduzir visualmente a tela de login do Spotify usando HTML semântico e CSS, construindo tudo a partir da observação da página original, sem copiar o código-fonte dela.

---

# Relatório de desenvolvimento

Registro do que foi feito em cada commit e do que a dupla entendeu em cada etapa, escrito ao longo do desenvolvimento.

## Commit 1 — Estrutura base do projeto

Qui 24/09 · Vitória

**O que foi feito:** Foi criado um novo repositório no Github, depois criamos os arquivos `index.html` e `style.css`. O `index.html` recebeu o `head` (charset, meta viewport, descrição, título, fonte Figtree e o link para o CSS) e o esqueleto semântico da página: `header` com o logo, `main` ainda vazio e `footer` com o aviso do reCAPTCHA. O `style.css` começou só com o comentário de abertura.

**O que entendemos:**

*Começamos apenas pelo HTML porque ele é como ossos para um site, a base de tudo. Já o CSS, seriam as roupas, acessórios, itens para embelezar...
*Usamos a meta viewport pois ela serve para fazer o site se adaptar corretamente ao tamanho da tela do celular. Sem ela, a página pode ficar toda desproporcional no celular, parecendo que foi feita para uma tela de computador, e aí o usuário precisa ficar dando zoom ou arrastando a tela para conseguir ver tudo.
*O `header` é a parte de cima da página, onde fica a logo do Spotify. O `main` é a parte principal, onde está o formulário de login e as opções para entrar na conta. Já o `footer` é a parte de baixo da página, onde ficam as informações sobre o reCAPTCHA, a Política de Privacidade e os Termos de Serviço.


## Commit 2 — HTML do cartão de login

Qui 24/09 · Vitória

**O que foi feito:** Montamos dentro do `main` a `section` do login: o título `h1`, a `nav` com os quatro links de login social em uma lista, o formulário com os campos de usuário e senha (cada um com seu `label`), o botão de mostrar senha com os dois ícones de olho em SVG, o checkbox "Lembrar de mim", o botão Entrar e os links de esqueci a senha e cadastro. Validamos o HTML no validator.w3.org.

**O que entendemos:**

*Colocamos os botões dentro de uma 'nav' e não em um 'form' porque esses botões são outras formas de entrar na conta, mas não fazem parte do formulário de login com e-mail e senha. Então, o `nav` serve para organizar essas opções de navegação.
*Quando clicamos no texto do `label`, o campo que está ligado a ele também é selecionado. Isso facilita bastante para quem usa celular ou tem alguma dificuldade para clicar diretamente no campo, além de ajudar leitores de tela.
*O `aria-describedby` serve para indicar uma informação relacionada ao campo, nesse caso, a mensagem de erro do campo. Já o `aria-pressed` indica se um botão está ativado ou não. No código, ele é usado no botão de mostrar a senha.


## Commit 3 — Imagens, variáveis, reset e cabeçalho

Sex 25/09 · Carol

**O que foi feito:** Adicionamos o logo e os ícones na pasta `imagens`. No CSS, criamos as variáveis no `:root` (cores tiradas da página original, fonte e medidas que se repetem, com 8px como unidade base de espaçamento), o reset com `box-sizing: border-box`, o `body` em flex de coluna, o foco visível para quem navega pelo teclado e o cabeçalho com o logo centralizado. Também tiramos o `role="switch"` do checkbox de lembrar de mim, porque o validador do W3C apontou erro por faltar o atributo `aria-checked`.

**O que entendemos:**

*Quando eu troquei o valor de `--cor-fundo`, a cor de fundo da página inteira mudou. A vantagem de usar variáveis é que fica mais fácil alterar uma cor ou outro valor em vários lugares do código de uma vez, sem precisar ficar procurando e mudando cada lugar separadamente.
*O `border-box` faz com que o tamanho definido para o elemento já inclua o `padding` e a borda. Já o `content-box`, que é o padrão, considera o tamanho apenas do conteúdo, então o padding e a borda aumentam o tamanho final do elemento.
*O `body` está usando `display: flex` e `flex-direction: column`, então os elementos ficam organizados um embaixo do outro, como uma coluna. Como o `body` ocupa no mínimo toda a altura da tela, o conteúdo consegue ocupar o espaço e o rodapé fica na parte de baixo.
*O `:focus` aparece sempre que um elemento recebe foco, enquanto o `:focus-visible` aparece principalmente quando o foco é importante para a navegação, como quando estamos usando o teclado. Isso deixa a página mais acessível sem ficar mostrando o contorno toda hora.


