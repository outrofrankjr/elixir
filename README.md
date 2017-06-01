#Elixir

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

![alt text](https://github.com/outrofrankjr/elixir/img/modointerativo.png "Modo interativo do Elixir")
