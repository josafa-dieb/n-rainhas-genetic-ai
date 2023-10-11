# n-rainhas-genetic-ai

## o poblema das n-rainhas
O problema da n-rainhas consiste em organizar n-rainhas em um tabuleiro n x n de uma forma em que as rainhas não se matem.

Exemplo: 5-rainhas, tabuleiro 5x5

|   | A | B | C | D | E |   |
|---|---|---|---|---|---|---|
| 1 | ♛ |   |   |   |   | 1 |
| 2 |   |   | ♛ |   |   | 2 |
| 3 |   |   |   |   | ♛ | 3 |
| 4 |   | ♛ |   |   |   | 4 |
| 5 |   |   |   | ♛ |   | 5 |
|   | A | B | C | D | E |   |

## Algoritmo: Genético
O algoritmo genético consite em uma forma de selecionar as melhores soluções em com
base na genética através de um cruzamento utilizando uma função de avalição para selecionar os melhores indivíduos de suas respectivas gerações.

1. Os primeiros indíviduos (população) serão gerados aleatoriamente
2. Será realziado o fitness avaliando os melhores indivíduos (função de avaliação)
3. Sera realizado a seleção dos indivíduos com o melhor grau de avaliação
4. Mutação e Cruzamento para gerar uma nova geração de indivíduo
5. Passar pelo critério de parada, se a solução ainda não é satisfatória execute os passos novamente.

![Fluxo algoritmo genético](https://computacaointeligente.com.br/assets/img/posts/GA/fluxograma.png)

# Modelagem do problema
Cada indivíduo será um tabuleiro preenchido com 1 e 0 referente a posição de cada rainha e espaços em brancos

### Exemplo: indivíduo 1:
[[0, 0, 0 , 1, 0],
[0, 0, 0 , 0, 1],
[0, 0, 1 , 0, 0],
[0, 0, 0 , 0, 1],
[0, 0, 0 , 0, 1]]

|   | A | B | C | D | E |   |
|---|---|---|---|---|---|---|
| 1 |   |   |   | ♛ |   | 1 |
| 2 |   |   |   |   | ♛ | 2 |
| 3 |   |   | ♛ |   |   | 3 |
| 4 |   |   |   |   | ♛ | 4 |
| 5 |   |   |   |   | ♛ | 5 |
|   | A | B | C | D | E |   |

### Exemplo: indivíduo 2:

[[0, 0, 1 , 0, 0],
[0, 0, 0 , 0, 1],
[1, 0, 0 , 0, 0],
[0, 1, 0 , 0, 0],
[0, 0, 1 , 0, 0]]

|   | A | B | C | D | E |   |
|---|---|---|---|---|---|---|
| 1 |   |   | ♛ |   |   | 1 |
| 2 |   |   |   |   | ♛ | 2 |
| 3 | ♛ |   |   |   |   | 3 |
| 4 |   | ♛ |   |   |   | 4 |
| 5 |   |   | ♛ |   | ♛ | 5 |
|   | A | B | C | D | E |   |


### Exemplo: cruzamento
[[0, 0, 0 , 1, 0],
[0, 0, 0 , 0, 1],
[1, 0, 0 , 0, 0],
[0, 1, 0 , 0, 0],
[0, 0, 1 , 0, 0]]


|   | A | B | C | D | E |   |
|---|---|---|---|---|---|---|
| 1 |   |   |   | ♛ |   | 1 |
| 2 |   |   |   |   | ♛ | 2 |
| 3 | ♛ |   |   |   |   | 3 |
| 4 |   | ♛ |   |   |   | 4 |
| 5 |   |   | ♛ |   |   | 5 |
|   | A | B | C | D | E |   |