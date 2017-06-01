# Elixir

## 1 Primeiros Passos

### 1.1 Instalando Elixir

O curso em questão usará máquinas Ubuntu 14.04.
para instalar Gvocê deve abrir o terminal e digitar os comandos:
Adicionando o Erlang Solutions repo:
`wget https://packages.erlang-solutions.com/erlang-solutions_1.0_all.deb && sudo dpkg -i erlang-solutions_1.0_all.deb`

`sudo apt-get update`

Instalando o Erlang e suas aplicações:
`sudo apt-get install esl-erlang`

Por fim, a instalação do Elixir:
`sudo apt-get install elixir`

As instruções de instalação para os demais sistema operacional poderá ser encontradas em [Elixir-lang.org](https://elixir-lang.org/) na aba [Install](https://elixir-lang.org/install.html).

### 1.2 Modo Interativo

Elixir vem com IEx, um console interativo, que nos permite avaliar expressões em Elixir.
Para iniciar, executamos `iex`:

![alt text](https://github.com/outrofrankjr/elixir/blob/master/img/modointerativo.png "Modo interativo do Elixir")


## 1.3 Aridade de funções

Aridade em linguagem funcionais corresponde ao número de argumentos que uma determinada função recebe.
No próprio terminal, voce pode consultar o `IEx.Helpers` (O módulo interativo de ajuda com o Elixir) que oferece auxílios durante o desenvolvimento e torna o terminal do Elixir mais prazeroso para o trabalho :smile:

Então, após execultar o comando `iex` digite um simples `h` que o IEX.Helpers explica:

* `b/1           - prints callbacks info and docs for a given module`
* `c/1           - compiles a file into the current directory`
* `c/2           - compiles a file to the given path`
* `cd/1          - changes the current directory`
* `clear/0       - clears the screen`
* `flush/0       - flushes all messages sent to the shell`
* `h/0           - prints this help message`
* `h/1           - prints help for the given module, function or macro`
* `i/1           - prints information about the data type of any given term`
* `import_file/1 - evaluates the given file in the shell's context`
* `l/1           - loads the given module's BEAM code`
* `ls/0          - lists the contents of the current directory`
* `ls/1          - lists the contents of the specified directory`
* `nl/2          - deploys local BEAM code to a list of nodes`
* `pid/1         - creates a PID from a string`
* `pid/3         - creates a PID with the 3 integer arguments passed`
* `pwd/0         - prints the current working directory`
* `r/1           - recompiles the given module's source file`
* `recompile/0   - recompiles the current project`
* `respawn/0     - respawns the current shell`
* `s/1           - prints spec information`
* `t/1           - prints type information`
* `v/0           - retrieves the last value from the history`
* `v/1           - retrieves the nth value from the history`


## 2 Coleções
### 2.1 Listas

Listas  são  um  tipo  de  coleção  de  elementos  e  podem conter diversos outros tipos dentro dela. Uma lista pode conter valores númericos, Strings e booleans, por exemplo.

Listas em Elixir, jamais podem ser comparadas  com  arrays  de Java ou PHP,  porque  não  os conceitos não são iguais. O conceito  aqui  é  que listas podem ter `head` (cabeça) e `tail` (cauda). A cabeça contém o  valor  e  a  cauda  por  si  mesma  é  a  lista  inteira.  Por  causa  dessa implementação, elas podem ser percorridas facilmente.

```elixir
iex> [3.14, :okgoogle, "AppleStore", true, 2]
[3.14, :okgoogle, "AppleStore", true, 2]
```

Elixir implementa listas como listas encadeadas. Isso significa que acessar a profundidade da lista é uma operação O(n). Por essa razão, é normalmente mais rápido inserir um elemento no início do que no final.

```elixir
iex> lista = [3.14, :pie, "Apple"]
[3.14, :pie, "Apple"]
iex> ["π"] ++ lista
["π", 3.14, :pie, "Apple"]
iex> lista ++ ["Cherry"]
[3.14, :pie, "Apple", "Cherry"]
```


#### Concatenação de listas

A concatenação de listas usa o operador ++/2.

```elixir
iex> [1, 2] ++ [3, 4, 1]
[1, 2, 3, 4, 1]
```

#### Subtração de listas

O suporte para subtração é provido pelo operador --/2; é seguro subtrair um valor que não existe:

```elixir
iex> ["foo", :bar, 42] -- [42, "bar"]
["foo", :bar]
```


Existem diversas funções para trabalhar com listas, você deve consultar  a  [documentação  oficial](https://elixir-lang.org/docs.html)  a  cada  atualização  da  linguagem para ficar por dentro de todas as novidades. :smile:

```elixir
iex> lista = [1,2,3]
[1,2,3]
iex> hd lista #acessando o head
1
iex> List.first lista #buscando a primeira posicao da lista
1
iex> newLista = List.insert_at lista, 3, 4 #inserindo o valor 4 na posição 3 da lista, salvando em uma nova lista
[1,2,3,4]
iex> newLista ++ lista #concatenando as duas listas
[1,2,3,4,1,2,3]
```


### 2.2 Tuplas

As tuplas são similares as listas porém são armazenadas de maneira contígua em memória. Isto permite acessar a sua profundidade de forma rápida porém sua modificação é custosa. A nova tupla deve ser armazenada inteira na memória. As tuplas são definidas com chaves.

```elixir
iex> {3.14, :okgoogle, "AppleStore", true, 2}
{3.14, :okgoogle, "AppleStore", true, 2}
```


Existem diversas funções para trabalhar com tuplas, você deve consultar  a  [documentação  oficial](https://elixir-lang.org/docs.html)  a  cada  atualização  da  linguagem para ficar por dentro de todas as novidades. :smile:

```elixir
iex> tupla = {3.14, :okgoogle, "AppleStore", true, 2}
{3.14, :okgoogle, "AppleStore", true, 2}
iex> tuple_size tupla #verificando o tamanho da tupla
5
iex> elem tupla, 2 #acessando o elemento no indice 2
"AppleStore"
iex> elem tupla, 4 #acessando o elemento no indice 4
2
iex> put_elem tupla, 0, 3 #atualizando o valor do indice zero
{3, :okgoogle, "AppleStore", true, 2}
```

### 2.3 Maps


## 3 Funções
### 3.1 Nomeadas

### 3.2 Privadas

### 3.3 Anônimas


## 4 Modulo


## 5 Structs

Structs são mapas especiais com um conjunto definido de chaves e valores padrões. Ele deve ser definido dentro de um módulo, no qual leva o nome dele. É comum para um struct ser a única coisa definido dentro de um módulo.

Para definir um struct nós usamos `defstruct` juntamente com uma lista de palavra-chave de campos e valores padrões:

```elixir
defmodule Example.User do
  defstruct name: "Sean", roles: []
end
```

Vamos criar algumas estruturas:

```elixir
iex> %Example.User{}
%Example.User{name: "Sean", roles: []}
```

```elixir
iex> %Example.User{name: "Steve"}
%Example.User{name: "Steve", roles: []}
```

```elixir
iex> %Example.User{name: "Steve", roles: [:admin, :owner]}
%Example.User{name: "Steve", roles: [:admin, :owner]}
```
Podemos atualizar nosso struct apenas como se fosse um mapa:

```elixir
iex> steve = %Example.User{name: "Steve", roles: [:admin, :owner]}
%Example.User{name: "Steve", roles: [:admin, :owner]}
iex> sean = %{steve | name: "Sean"}
%Example.User{name: "Sean", roles: [:admin, :owner]}
```
Mais importante, você pode associar estruturas contra mapas:

```elixir
iex> %{name: "Sean"} = sean
%Example.User{name: "Sean", roles: [:admin, :owner]}
```


## 6 Lazy Evaluation


## 7 Recursividade


## 8 Mix
