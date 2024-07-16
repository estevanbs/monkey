# Lexer

Sua função é facilitar trabalhar com o código-fonte durante processo de compilação.

Esse lexer transforma o código-fonte em uma sequência de tokens 

    código-fonte -> tokens

Tokens são pequenos e fáceis de reconhecer, e são posteriormente enviados ao parser para serem transformados em um *abstract syntax tree (ast)*.

Em monkey, espaços em branco são utilizados meramente para separar tokens, e o comprimento deles é irrelevante. Por isso, o lexer ignora o comprimento dos espaços em branco.

Lexers utilizados em linguagens comerciais geralmente anexam ao token o número da linha, da coluna, e o nome do arquivo referente a ele. O lexer de monkey não faz isso.

Os tipos atribuídos aos tokens por esse lexer são:

| Tipo atribuído | Descrição                                           | Exemplo de literal | Tipo do token     |
|----------------|-----------------------------------------------------|--------------------|-------------------|
| ILLEGAL        | Caracteres ilegais (não reconhecidos pelo lexer)    |                    | Especial          |
| EOF            | Final do arquivo                                    |                    | Especial          |
| IDENT          | Identificadores de variáveis                        | result             | Operador          |
| INT            | Números inteiros                                    | 1                  | Operador          |
| ASSIGN         | Operador de atribuição                              | =                  | Delimitador       |
| PLUS           | Operador de soma                                    | +                  | Delimitador       |
| COMMA          | Separador de identificador                          | ,                  |                   |
| SEMICOLON      | Separador de declaração (geralmente final de linha) | ;                  |                   |
| LPAREN         | TODO                                                | (                  |                   |
| RPAREN         | TODO                                                | )                  |                   |
| LBRACE         | TODO                                                | {                  |                   |
| RBRACE         | TODO                                                | }                  |                   |
| FUNCTION       | Utilizado na declaração de função                   | fn                 | Palavra reservada |
| LET            | Utilizado na declaração de variável                 | let                | Palavra reservada |

O input desse lexer é uma string.

Para retornar a lista de tokens, é necessário chamar a função NextToken(). Ela retorna um token por vez que é chamada.



