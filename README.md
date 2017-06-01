# Elixir

## Primeiros Passos

### Instalando Elixir

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

### Modo Interativo

Elixir vem com IEx, um console interativo, que nos permite avaliar expressões em Elixir.
Para iniciar, executamos `iex`:

![alt text](https://github.com/outrofrankjr/elixir/blob/master/img/modointerativo.png "Modo interativo do Elixir")


## Aridade de funções

Aridade em linguagem funcionais corresponde ao número de argumentos que uma determinada função recebe.

* `b/1           - Imprime callbacks de informações e documentos para um determinado módulo`
* `c/1           - Compila um arquivo no diretório atual`
* `c/2           - Compila um arquivo para o caminho dado`
* `cd/1          - Altera um diretório atual`
* `clear/0       - Limpa o terminal`
* `flush/0       - Apagar todas as mensagens enviadas ao shell`
* `h/0           - Imprime a interação com a ajuda`
* `h/1           - Imprime ajuda para o módulo, função ou macro fornecidos`
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


## Coleções
### Listas

### Tuplas

### Palavras-chave

### Maps


## Funções
### Nomeadas

### Privadas

### Anônimas


## Modulo


## Lazy Evaluation


## Structs


## Recursividade
