# Projeto de Grafos em Java

Projeto didático desenvolvido para as aulas de **Estrutura de Dados II - Sistemas de Informação** no **Instituto Federal do Sul de Minas (IFSULDEMINAS)**.

O programa representa cidades como vértices de um grafo e as ligações entre elas como arestas com pesos. A distância entre as cidades é informada em quilômetros, permitindo comparar como os dados e os algoritmos de grafos podem ser utilizados em situações práticas, como rotas e conexões.

## Objetivo educacional

O projeto apresenta os principais conceitos de grafos por meio de uma aplicação de console:

- vértices e arestas;
- grafos direcionados e não direcionados;
- representação por listas de adjacência;
- inclusão de vértices e arestas;
- percurso em largura (BFS);
- percurso em profundidade (DFS);
- verificação de alcance entre vértices;
- menor caminho com o algoritmo de Dijkstra;
- uso de arquivos CSV como fonte de dados.

## Funcionalidades

Ao iniciar o programa, o usuário escolhe entre:

1. Grafo não direcionado.
2. Grafo direcionado.

Em seguida, o sistema carrega as cidades e suas ligações dos arquivos `cidades5.csv` e `arestas5.csv` e apresenta um menu com as seguintes opções:

- adicionar uma nova cidade;
- adicionar uma ligação entre duas cidades;
- mostrar o grafo e suas adjacências;
- verificar o alcance entre duas cidades;
- executar uma busca em profundidade (DFS);
- executar uma busca em largura (BFS);
- calcular o menor caminho com Dijkstra.

As cidades são identificadas pelo CEP. Dessa forma, o CEP funciona como chave para localizar cada cidade no `HashMap` usado pelo programa.

## Estrutura do projeto

| Caminho | Responsabilidade |
| --- | --- |
| `src/App.java` | Interface de console, carregamento dos dados e menu principal |
| `src/Grafo.java` | Implementação genérica do grafo e listas de adjacência |
| `src/Aresta.java` | Representa uma ligação e seu peso |
| `src/Cidade.java` | Representa uma cidade e implementa comparações e igualdade pelo CEP |
| `src/DistanciaNode.java` | Estrutura auxiliar utilizada na implementação de menor distância |
| `cidades5.csv` | Dados iniciais das cidades |
| `arestas5.csv` | Dados das ligações e pesos |
| `lib/` | Bibliotecas externas do projeto |
| `bin/` | Arquivos Java compilados |

O projeto também possui conjuntos adicionais de dados: `cidades.csv`, `arestas.csv`, `arestas-full.csv` e `arestas-exemplo1.csv`. Eles podem ser utilizados para diferentes testes e exercícios.

## Formato dos arquivos CSV

Cada linha de `cidades5.csv` contém o nome da cidade, o estado e o CEP:

```text
Machado,MG,111
Poços de Caldas,MG,333
```

Cada linha de `arestas5.csv` contém os CEPs de origem e destino e o peso da ligação:

```text
111,333,85
111,222,33
```

No exemplo acima, existe uma conexão entre Machado e Poços de Caldas com peso 85, e entre Machado e Alfenas com peso 33.

## Exercício em sala

O código contém partes em comentários para serem usadas como atividade prática. O objetivo é completar a implementação das operações declaradas em `Grafo.java`, como alcance, DFS e BFS, e ativar as respectivas chamadas no menu de `App.java`.

Entre os pontos de aprendizagem estão:

- preencher lacunas em algoritmos de grafos;
- usar fila para implementar BFS;
- usar recursão para implementar DFS;
- controlar vértices já visitados;
- percorrer uma lista de adjacência;
- adaptar o grafo para situações direcionadas e não direcionadas.
