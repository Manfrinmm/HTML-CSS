# Categorias

## Texto

### Observações
Não se se cabe aqui ou em algum outro lugar, mas deixo anotado aqui:

- Com o HTML5, vários atributos foram descontinuados, sendo agora indicado o uso de CSS para ter efeito semelhante. 
- A unidade `em` é usada em CSS como medida relativa, variando de tela para tela, sempre levando em consideração que `1em` é igual à altura da fonte padrão do texto. 
- Da mesma forma, `ex` é uma unidade relativa à altura da letra `x` minúscula. 
- Sugiro colocarmos uma uma seção para "atributos globais" e outra para "atributos de evento".
- Tags de texto como `<b>`, `<i>` e `<u>` só afetam a aparência e não tem a semântica, por isso são chamadas de 'presentational elements' e devem ser evitados.
- HTML5 redefiniu as três tags acima com um papel semântico não muito claro.
- `<u>` em especial (underline) deve ser evitado por estar tradicionalemnte associada a links.
- Eu não sabia da existência das phrase tags; são muito importantes na semântica. Talvez caiba uma subseção, já vou deixá-las em ordem.
- Phrase tag são tags usadas para indicar que um bloco de texto tem significado estrutural.
- Ainda na linha da observação anterior, talvez tenhamos que colocar nossa pesquisa dentro de outro contexto: https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Content_categories#Phrasing_content
- Sugiro mudarmos o nivelamento de cada tag para `###` em vez de `-`, para que apenas as propriedades fiquem itemizadas e fique mais fácil encontrar as tags. De qq forma, é só uma sugestão, se não quiserem, sem problema.
- Dou a mesma sugestão para as partes do texto, para diminuir a profundidade das listas em cada tag. Exemplo na tag `em` abaixo.

### `<p>`
- `<p>`
  - Semântica: Um parágrafo como bloco no texto. Todo parágrafo deve vir dentro de um elemento `<p>`.
  - Atributos
    - `align` foi descontinuado no HTML5, em favor do CSS: `<p style="text-align:right"> parágrafo </p>`
    - Margens (atributo CSS): 
        - margin-top: 1em;
        - margin-bottom: 1em;
        - margin-left: 0;
        - margin-right: 0;
    - `display` (default:block); O atributo CSS block mostra um elemento como um bloco no texto, ou seja, começa numa nova linha e ocupa toda a largura disponível.

### `<h1> -> <h6>`
- `<h1> -> <h6>`
    - Semântica: Estes são os títulos disponíveis, do mais importante (`<h1>`) até o de destaque pouco maior que o texto (`<h6>`). 
    - Sintaxe: `<h1> Título </h1>`
    - Defaults (CSS):
        - h1 {
                display: block;
                font-size: 2em;
                margin-top: 0.67em;
                margin-bottom: 0.67em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        - h2 {
                display: block;
                font-size: 1.5em;
                margin-top: 0.83em;
                margin-bottom: 0.83em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        - h3 {
                display: block;
                font-size: 1.17em;
                margin-top: 1em;
                margin-bottom: 1em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        - h4 {
                display: block;
                font-size: 1em;
                margin-top: 1.33em;
                margin-bottom: 1.33em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        - h5 {
                display: block;
                font-size: .83em;
                margin-top: 1.67em;
                margin-bottom: 1.67em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

        - h6 {
                display: block;
                font-size: .67em;
                margin-top: 2.33em;
                margin-bottom: 2.33em;
                margin-left: 0;
                margin-right: 0;
                font-weight: bold;
                }

    - Observações: 
        - Todo título de seção, subseção, etc, deve vir dentro de algum destes elementos.
        - Não importa o nível de título que você escolha usar, desde que a hierarquia entre eles faça sentido (jamais use um `<h2>` como subseção de um `<h3>`)
        - Use apenas um `<h1>` por página
        - Dos 6 títulos disponíveis, tente usar no máximo 3 por página.


### `<span>`
- `<span>`
    - Semântica: Este elemento não tem semântica definida, é apenas parte (inline) de um texto que pode ser alterada posteriormente via CSS.

### `<br>`
- `<br>`
    - Semântica: Quebra de linha. Quebra a linha atual e continua o texto numa nova linha dentro do elemento `<p>`, sem a necessidade de se criar um novo parágrafo.
    - Sintaxe: Não precisa de closing tag.
    - Observações: 
        - Jamais use esta tag para separar parágrafos.
        - Jamais use para aumentar o espaçamento entre linhas, para isso use CSS (elemento margin ou p)
    - Atributos:
        -  

### `<em>` Ênfase

#### Semântica
Esta phrase tag dá ênfase a uma palavra, sendo reconhecida por leitores de tela e lida em tom diferente. 

#### Observações
Apesar de ser padrão nos browsers estilizar `em` como itálico, você não deve usá-la para colocar um texto em itálico. Para isso, use CSS ou a tag `<i>`.

---

### `<mark>` Highlight

#### Semântica
Phrase tag usada para destacar texto via highlight. 

#### Sintaxe
`<mark> highlight em HTML </mark>`

#### Defaults
mark {
  background-color: yellow;
  color: black;
}

----

### `<strong>` Importante

#### Semântica
Phrase tag usada para dar importância a uma parte do texto. 

#### Sintaxe
`<strong>Strong text</strong>`

#### Defaults
strong {
  font-weight: bold;
}

#### Observações
Apesar de ser padrão nos browsers estilizar `strong` como negrito, você não deve usá-la para colocar um texto em negrito. Para isso, use CSS ou a tag `<b>`.

----
### `<abbr>` Abreviação

#### Semântica
Phrase tag usada para indicar abreviação. 

#### Sintaxe
<abbr title = "Rowan Atkinson">Mr. Bean</abbr>

#### Defaults
strong {
  font-weight: bold;
}

#### Atributos
    - title: é mostrado quando o mouse passa sobre a abreviação

----

### `<dfn>` Definição

#### Semântica
Phrase tag usada para indicar que naquele local fica a definição da palavra.

#### Sintaxe
<dfn>HTML</dfn>

#### Defaults
strong {
  font-weight: bold;
}

#### Atributos
- `title` é o termo a ser definido, da forma como será reconhecido por buscas e leitores
- 

#### Observações
- O elemento "parent" mais próximo, seja ele  `<p>`, `<dt>`, `<dd>` ou `<section>`  deve ser a definição do termo em si.
- Por ser a definição, é indicado que esta tag seja usada na primeira vez que a palavra é usada, quando seu significado é dado.

---

### `<blockquote>` Citação

#### Semântica
Phrase tag usada para indicar uma citação extendida de uma outra fonte. 

#### Sintaxe
<blockquote cite="http://www.google.com">
Texto da citação de outro site.
</blockquote>

#### Defaults
blockquote {
  display: block;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 40px;
  margin-right: 40px;
}

#### Atributos
cite é um atributo cujo valor é uma url, indicando a fonte da citação.

#### Observações
Use a tag `<q>` para citações curtas (inline).

---
### `<code>` Código

#### Semântica
Phrase tag usada para indicar que o texto é um código em alguma linguagem de programação ou marcação. 

#### Sintaxe
`<code><?php echo "Hello World!" ?></code>`

#### Defaults
code {
  font-family: monospace;
}

#### Observações
O elemento `<code>` é usado para uma linha de código. Para mais linhas, envolva o `<code>` dentro de um elemento `<pre>`.

---

### `<kbd>` Teclado

#### Semântica
Phrase tag usada para dar importância a uma parte do texto. 

#### Sintaxe
`<strong>Strong text</strong>`

#### Defaults
strong {
  font-weight: bold;
}

#### Observações
Apesar de ser padrão nos browsers estilizar `strong` como negrito, você não deve usá-la para colocar um texto em negrito. Para isso, use CSS ou a tag `<b>`.


## Entrada de dados

## Bloco
