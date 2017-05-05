# Introduction to Data Structures
## Vídeo 1: Introduction to data structures

### Objetivo: Introduzir os conceitos básicos de estruturação de dados

* Quando se trabalha com um conjunto de dados, o modo como armazenamos, organizamos e agrupamos os dados importa muito.

* É o modo como armazenamos e organizamos dados em um computador, de modo que os mesmos possam ser usados de forma eficiente. 
* Duas formas de estudar estruturas de dados:

** Modelos lógicos e matemáticos (abstract data types - ADT) - visão abstrata dos dados, "high level" view, suas operações, etc. Ex: armazenar determinados dados em uma lista e ler tais dados por suas posições na lista ou modificar elementos da lista com base em sua posição.

** Implementação - modos concretos de visualizar os dados.

** ADT: definimos os dados e as operações, mas nenhuma implementação destes dados. Analisamos a estrutura lógica dos dados, as operações disponíveis, os custos destas operação (em termos de tempo) e sua implementação em uma dada linguagem de programação

## Vídeo 2: Data Structures: List as abstract data type

* Listas como um ADT: 
** armazenar elementos de um mesmo tipo, ler e modificar elementos em determinada posição. Arrays são exemplos de listas
** Dica: quando trabalhamos com lista de modo que o tamanho desta lista é completamente preenchido por dados, podemos copiar estes dados e jogá-los em uma nova lista com o dobro do tamanho da lista e liberar memória usada na lista anterior.
** Custos em termos de tempo de certa operações em uma lista dinâmica:
 *** Access (ler/ escrever elementos em certa posição) - custo constante em termos de tempo (O(1))
 *** Inserir/ Remover/ Adicionar elementos - custo proporcional ao tamanho da lista (O(n))
 
## Vídeo 3: Introduction to linked list
* Para compreender bem listas linkadas, precisamos entender muito bem as limitações de se utilizar arrays.
** Em uma arquitetura comum, um variável do tipo integer consome 4 bytes de memória. Logo, um Array 4 quatro elemntos integer consumiria um bloco contínuo de memória de tamnho 16 bytes.
** Se quisermos aumentar o tamanho deste array, o computador não consegue simplesmente amplicar a memória alocada ao Array inicial com as memórias adjacentes ao bloco e por isso precisa criar uma nova array com um tamanho maior e copiar os dados originais neste novo bloco. Aqui, existe um problema, se separarmos mais memória que o necessário para o manuseio do Array (criando um array com tamanho muito maior que o necessário), a memória do computador estará sendo alocada de maneira pouco eficiente, por outro lado, se criarmos um array pequeno (de modo a precisar incluir novos elementos futuramente), precisaremos repetir o processo de criar um array completamente novo para alocar os dados antigos neste novo bloco de memória.
** A solução para este problema são as listas linkadas: ao invés de alocar um grande bloco único de memória para o array todo, é possível fazer requests para cada elemento do array separadamente. Cada elemento é armazenado em pedaços não contínuos de memória, neste caso, juntamente com um outro pedaço de memória alocado a ele que indica o endereço da memória com o próximo pedaço do Array. 
** Ao invés de pedir ao computador para alocar um array todo, solicitamos que ele aloque um bloco com duas variáveis: a integer e um pointer (que aponta para o próximo bloco de memória do array).
