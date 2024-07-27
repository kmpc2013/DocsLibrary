---
tags:
  - HTML5
  - Markdown
---


# Markdown - Comandos básicos
> Markdown é uma linguagem de marcação leve, amplamente utilizada para formatar texto de forma simples e legível, tanto em sua forma "bruta" quanto quando convertida para HTML ou outros formatos. Criada por John Gruber e Aaron Swartz, o objetivo principal do Markdown é permitir que documentos de texto sejam facilmente legíveis e editáveis, enquanto ainda podem ser convertidos para uma apresentação mais rica.

---

<a name="secao-titulacao"></a>
<h2>Titulação</h2>
A titulação em Markdown é usada para definir diferentes níveis de cabeçalhos, que são essenciais para organizar o conteúdo de forma hierárquica e facilitar a leitura. Em Markdown, os cabeçalhos são criados usando o símbolo de hashtag (#). Dependendo do número de hashtags usadas, você pode definir cabeçalhos de diferentes níveis.
Além de hashtags, alguns editores de Markdown suportam a titulação HTML "h1, h2, h3, ...":

~~~markdown title="Código"
# Título 1
<h1> Título 1 </h1>
[...]
###### Título 6
<h6> Título 6 </h6>
~~~
!!! note "Retorno"

    # Título 1
    <h1> Título 1 </h1>
    [...]
    ###### Título 6
    <h6> Título 6 </h6>

<a name="secao-enfase"></a>
<h2>Ênfase</h2>
A ênfase em Markdown é usada para aplicar formatação especial ao texto, como itálico e negrito:

~~~markdown title="Código"
*texto em itálico*
_texto em itálico_
**texto em negrito**
__texto em negrito__
***texto em itálico e negrito***
___texto em itálico e negrito___
~~~
!!! note "Retorno"
    *texto em itálico*

    _texto em itálico_

    **texto em negrito**

    __texto em negrito__

    ***texto em itálico e negrito***

    ___texto em itálico e negrito___


<a name="secao-links"></a>
<h2>Links</h2>
Os links em Markdown permitem que você crie hiperlinks de maneira simples e legível:

~~~markdown title="Código"
[Texto do Link](http://exemplo.com)
[Texto do Link](http://exemplo.com "Título do Link")
<http://exemplo.com>
[![Texto Alternativo da Imagem](http://exemplo.com/imagem.png)](http://exemplo.com)
[texto do link]: http://exemplo.com "Título Opcional"
Este é um [link de referência][texto do link].
~~~
!!! note "Retorno"
    [Texto do Link](http://exemplo.com)
    
    [Texto do Link](http://exemplo.com "Título do Link")
    
    <http://exemplo.com>
    
    [![Texto Alternativo da Imagem](http://exemplo.com/imagem.png)](http://exemplo.com)
    
    [texto do link]: http://exemplo.com "Título Opcional"
    
    Este é um [link de referência][texto do link].

<a name="secao-ancoras"></a>
<h2>Âncoras</h2>
Âncoras em Markdown permitem criar links internos dentro de um documento, facilitando a navegação para diferentes seções. Elas são especialmente úteis em documentos longos com várias seções, como tutoriais, manuais e guias.
Para isso, caso esteja utilizando titulos com "#" os IDs são criados seguindo as seguintes métricas:

- Espaços são substituídos por hífens (-).
- Todos os caracteres são convertidos para minúsculas.
- Caracteres especiais (exceto hífens) são removidos.

Caso esteja utilizando "<h1\>" pode utilizar a tag "name" para definir o ID, por exemplo `<h1 name="secao-name">TITULO</h1>"`:

~~~markdown title="Código"
- [Seção titulação](#secao-titulacao)
- [Seção ênfase](#secao-enfase)
- [Seção links](#secao-links)
~~~
!!! note "Retorno"
    - [Seção titulação](#secao-titulacao)
    - [Seção ênfase](#secao-enfase)
    - [Seção links](#secao-links)

<a name="secao-listas"></a>
<h2>Listas</h2>
listas são uma maneira prática de organizar informações em um formato estruturado. Existem dois tipos principais de listas que você pode criar: listas ordenadas e listas não ordenadas:

<h3>Listas Não Ordenadas:</h3>
Você pode criar listas não ordenadas usando asteriscos (*), hífens (-) ou sinais de mais (+). Todos funcionam da mesma maneira.


~~~markdown title="Código"
- Item 1
- Item 2
  - Subitem 1
  - Subitem 2
~~~
!!! note "Retorno"
    - Item 1
    - Item 2
        - Subitem 1
        - Subitem 2
  
<h3>Listas Ordenadas:</h3>
Listas ordenadas são usadas quando a ordem dos itens é importante. Elas são criadas usando números seguidos por um ponto (.).
~~~markdown title="Código"
1. Primeiro item
2. Segundo item
   1. Subitem 1
   2. Subitem 2
3. Terceiro item
~~~
!!! note "Retorno"
      1. Primeiro item
      2. Segundo item
         1. Subitem 1
         2. Subitem 2
      3. Terceiro item

<a name="secao-citacoes"></a>
<h2>Citações</h2>
São usadas para destacar texto, como trechos de artigos, livros, ou qualquer outra fonte de informação. Elas são especialmente úteis para referências, comentários ou notas adicionais:
~~~markdown title="Código"
> ### Titulo de citação
> Este é um nível de citação.
>> Este é um nível aninhado de citação.
~~~
!!! note "Retorno"
    > ### Titulo de citação
    > Este é um nível de citação.
    >> Este é um nível aninhado de citação.

<a name="secao-codigo"></a>
<h2>Código</h2>
Inserir código em Markdown é bastante simples e pode ser feito de duas maneiras principais: código inline e blocos de código:
~~~markdown title="Código"
Para exibir `código inline`, use crases simples.
```
Para exibir multiplas
linhas
de
código
use trés crases
```
``` python title="Código"
# Pode colocar a linguaguem ao lado das crases 
# para habilitar a coloração e 
# a tag "title" para definir o titulo.
def funcao():
  print("string")
```
~~~
!!! note "Retorno"
    Para exibir `código inline`, use crases simples.
    ```
    Para exibir multiplas
    linhas
    de
    código
    use trés crases
    ```
    ``` python title="Código"
    # Pode colocar a linguaguem ao lado das crases 
    # para habilitar a coloração e 
    # a tag "title" para definir o titulo.
    def funcao():
      print("string")
    ```

<a name="secao-tabelas"></a>
<h2>Tabelas</h2>
são uma maneira eficaz de organizar e apresentar dados de forma clara e estruturada. A sintaxe é simples e permite criar tabelas com cabeçalhos, colunas e linhas.
Uma tabela em Markdown é criada usando pipes (|) para separar colunas e hifens (-) para separar os cabeçalhos das linhas da tabela.
Você pode controlar o alinhamento das colunas usando dois pontos (:) nos hifens:
- Alinhamento à esquerda: :---
- Alinhamento ao centro: :---:
- Alinhamento à direita: ---:
As tabelas podem incluir linhas de cabeçalho, e você pode adicionar múltiplas linhas se necessário. A estrutura permanece a mesma.

~~~markdown title="Código"
| Fruta    | Cor      | Quantidade |
|:---------|:--------:|-----------:|
| Maçã     | Vermelha |         10 |
| Banana   | Amarela  |          6 |
| Laranja  | Laranja  |          8 |
~~~
!!! note "Retorno"
    | Fruta    | Cor      | Quantidade |
    |:---------|:--------:|-----------:|
    | Maçã     | Vermelha |         10 |
    | Banana   | Amarela  |          6 |
    | Laranja  | Laranja  |          8 |


<a name="secao-linhas"></a>
<h2>Linhas</h2>
linhas são usadas para criar separadores ou dividir o conteúdo visualmente:

- Três ou mais asteriscos (***)
- Três ou mais hifens (---)
- Três ou mais underlines (___)

~~~markdown title="Código"
---
___
~~~
!!! note "Retorno"
    ---
    ___
