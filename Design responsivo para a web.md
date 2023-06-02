# freeCodeCamp | Design responsivo para a web

## HTML moderno

- As tags html sempre começam com `<tag>` e terminam com `</tag>`. O texto que vai no meio é identificado pela tag.
	- *Atributos* são palavras especiais usadas dentro da tag de abertura de um elemento para controlar o comportamento dele.
		- O atributo `id` é utilizado para identificar elementos HTML específicos. Esse valor deve ser único no documento.
- **Títulos** são colocados em html com as tags `<h1>` até `<h6>`. Quanto menor o número depois do 'h' menor a importância do texto.
- **Parágrafo** é criado utilizando o elemento `<p>`.
- **Comentários** são partes do código que não são renderizadas e por isso só servem para deixar uma mensagem para seu eu do futuro ou para outros programadores. Muitas vezes são usados para *inativar* uma parte do seu código. Para escrever códigos faça: `<!-- comentário -->`
- O HTML5 tem alguns elementos que identificam diferentes áreas de conteúdo. Essas elementos tornam seu HTML mais fácil de ler e ajudam com a otimização dos mecanismos de busca (SEO) e com a acessibilidade.
	- A tag `<main>` geralmente indica a seção principal da página.
	- A tag `<section>` é usada para separar conteúdos diferentes.

>BOA PRÁTICA: Deixar o código aninhado facilita a leitura e a manutenção do seu código. O espaçamento padrão é de 2 espaços.

- **Imagens** são adicionadas por meio da tag `<img>`. Essa tag é diferente pois *não possui tag de fechamento*.
	- A tag `img` possui o atributo `src` que especifica o URL da imagem. Exemplo: `<img src="caminho-do-arquivo.jpg">`.
	- Todas os elementos `img` devem ter um atributo `alt` que deve incluir um texto que explica a imagem. Esse texto é usado tanto para ser exibido quando a imagem não é carregada como para fins de acessibilidade para leitores de tela.
	- A tag `<figure>` representa um conteúdo auto-contido e permitirá que você associe uma imagem com uma legenda. A tag `<figcaption>` adiciona uma legenda para a imagem e deve ser colocada dentro da tag `figure`.
- **Links** são formas de referenciar outras páginas e conteúdos. Ele é criado utilizando a tag `<a>` com o atributo `href` especificando a página-alvo. Exemplo: `<a href="outra-pagina.com"></a>`.
	- O texto do link deve ser colocado entre a tag de abertura e de fechamento.
	- O atributo `target` especifica como o navegador vai abrir o link. O valor `_blank_` faz com que o conteúdo do link seja aberto em outra página.
	- Qualquer elemento pode se tornar um link, desde que a tag `a` *cubra* esses elementos.
- **Listas não ordenadas** (ou bullet lists) são criadas utilizando a tag `<ul>` e dentro dessa tag utilizar as tags `<li>` para criar os itens da lista. Exemplo:

```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

- **Listas ordenadas** (ou listas numeradas) são semelhantes às listas não ordenadas, porém utilizam a tag `<ol>`
- Para **enfatizar** texto utilize a tag `<em>`. Para mostrar que o texto é **Importante/urgente** utilize a tag `<strong>`.
- **Formulários** são criados dentro da tag `<form>`. Dentro da tag, utilize o atributo `action` especificando o caminho para onde os dados serão enviados. Exemplo: `<form action="/submit-url"></form>`
	- Para que os dados de um formulário sejam acessados pelo local especificado no atributo `action`, você deve dar ao campo de texto um atributo `name` e atribuir a ele um valor que represente os dados que estão sendo enviados. Exemplo: `<input type="text" name="email">`.
	- O texto de placeholder é usado para dar às pessoas uma dica sobre o tipo de informação que deve ser inserido em uma entrada (input). Por exemplo, `<input type="text" placeholder="Email address">`.
	- Para evitar que um usuário envie o formulário quando as informações necessárias estiverem faltando, você precisa adicionar o atributo `required` a um elemento `input`. Não há a necessidade de definir um valor para o atributo `required`. Em vez disso, apenas adicione a palavra `required` (obrigatório) ao elemento `input`, certificando-se de que haja um espaço entre esse atributo e os outros.
	- Para **coletar dados** utilize o elemento `<input>` que são de fechamento automático.  O atributo `type` vai indicar que tipo de dado o `input` vai extrair do usuário.
		- Uma forma de identificar elementos `input` são por meio dos elementos `label` que são usados para ajudar a associar o texto de um elemento `input` com o próprio elemento `input` (especialmente para tecnologias assistivas como leitores de tela). Você deve fazer com que o `label` enlace o input junto com o texto.
		- Existe uma outra forma de associar o texto de um elemento `input` com o elemento em si, que é utilizando a tag `label` junto com o atributo `for` usando o mesmo valor que o atributo `id` do elemento `input`.
			- Outra forma é utilizando o atributo `id`.
		- `type="text"`: Cria um campo de texto para obter a entrada de texto de um usuário.
		- `type="radio"`: Cria um botão de opção onde o usuário só poderá escolher uma dentre muitas.
			- Para fazer com que selecionar um botão de opção automaticamente desmarque a seleção do outro, os dois botões devem ter um atributo de `name` com o mesmo valor.
			- Os dados de formulário para o botão são baseados em seus atributos `name` e `value`.
		- `type="checkbox"`: Caixa de seleção para perguntas que tenham mais de uma resposta.
	- Para criar **botões** utilize a tag `<button>`. O texto entre a abertura e o fechamento da tag é o texto que aparece dentro do botão.
		- O comportamento padrão de clicar em um botão de formulário sem qualquer atributo envia o formulário para o local especificado no atributo `action`. Apesar disso, é sempre bom adicionar o atributo `type` com o valor `submit` ao `button` para deixar claro que ele é um botão de envio.
	- O elemento `fieldset` é usado para **agrupar inputs e labels** relacionados em um formulário da web. Os elementos `fieldset` são elementos de nível de bloco, o que significa que eles aparecem em uma nova linha.
		- O elemento `legend` atua como uma legenda para o conteúdo do elemento `fieldset`. Ele dá aos usuários um contexto sobre o que devem inserir nessa parte do formulário.