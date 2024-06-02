# Trabalho Prático 3 de AEDS3!

Para esse trabalho, implementamos backups compactados pelo algoritmo LZW no código do TP2 


# Métodos e Classes Criadas

**Método:** Descrição



## Perguntas

**-   PERGUNTA**
RESPOSTA


# Métodos que estavam no TP2

**Menu na Main:** Menu na main que opera pela estrutura condicional switch case no console dando as opções de: inserir novo registro, buscar uma chave, deletar um registro e atualizar um registro para o usuário.
ATENÇÃO!!! A opção do menu não lida muito bem com acentuação, adicionamos um procedimento para execução dos comandos normalmente (sem menu)

**Classe ArquivoLivros:** Criamos essa classe para que tivessemos uma classe de arquivos não genérica, visto que o TP2 pede uma lista invertida de Livros

**Método Tamanho na classe Arquivo:** Adicionamos esse método para recuperar o último id do arquivo ( apenas para debug mesmo )

**Método Create na classe ArquivoLivros:** Neste método, criamos o objeto de livro no arquivo principal normalmente e, depois, criamos um índice para cada palavra do título do livro com base no id recebido pelo método create principal, para fazer isso, partimos o titulo em cada espaço, depois removemos pontos (tipo: ; : ! ? . , ) e utilizamos toLowerCase() para normalizar a palavra

**Método Update na classe ArquivoLivros:** Neste método, fazemos um update de um livro no arquivo principal normalmente, depois deletamos todos os indices da lista invertida que estavam associados ao título antigo e, por fim, adicionamos os indices do título novo do livro.

**Método Delete na classe ArquivoLivros:** Neste método, fazemos a deleção de um livro no arquivo principal normalmente e, depois, deletamos as palavras da listaInvertida associadas ao livro deletado uma por uma

**Método LimparString na classe ArquivoLivros:** Fiz esse método para melhorar na praticidade de limpar as strings, adicionei, também, a funcionalidade de remoção da acentuação

**Método Limpar na classe ArquivoLivros:** Esse método é auxiliar para o Read, ele quebra uma string em todos os espaços (" "), resultando um array de strings, depois remove pontos (tipo: ; : ! ? . , ) e utiliza toLowerCase() para normalizar a palavra. Por fim, o método checa se foi existem stopwords no array e as remove.

**Método de União na classe ArquivoLivros:** Esse método é responsável por realizar a união descrita no método READ, se ele receber os conjuntos (2,3,5) e (1,3,5), vai retornar (3,5) 

**Método Read na classe ArquivoLivros:** Neste método, recebemos uma string por parametros e separamos elas nos espaços em branco e depois limpamos ela, isso nos retorna um array de strings, se o array de strings conter apenas uma palavra, nós simplesmente fazemos uma pesquisa pelos livros que contém essa palavra e retornamos isso. Se o array conter mais de uma palavra, fazemos a união do conjunto de livros que possui cada uma das palavras. **Exemplo:** 
|Palavra| Livros  |
|--|--|
| Dados | 1, 2, 4  |
| Algoritmo | 1, 3, 4  |

Fazemos a união dos dois conjuntos e temos os livros 1 e 4, se adicionarmos a palavra abaixo:
|Palavra| Livros  |
|--|--|
| Estrutura | 4  |


Fazemos a união do conjunto 1 e 4 com o conjunto de Estrutura, resultando no livro 4 apenas.

**Método getStopwords na classe ArquivoLivros:** Baixamos um dataset com inúmeras stopwords (em português) do site Kaggle (https://www.kaggle.com/datasets/heeraldedhia/stop-words-in-28-languages), a função getStopwords pega todas as Stopwords no arquivo baixado e coloca em um ArrayList

**Método DEBUG:** Um método que criamos para printar todos os registros no arquivo principal e na lista invertido, só para ter certeza que está tudo nos conformes
