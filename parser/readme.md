# Parser

Sua função é construir uma estrutura hierárquica dos tokens mapeados pelo lexer.

Esse parser cria uma *abstract syntax tree (ast)* dos tokens

    tokens -> ast

O processo realizado pelo parser também é chamado de análise sintática.

Esse parser é um recursive descent (top-down) operator precedent parser, também chamado de Pratt Parser, criado por Vaughan Pratt.

 - top-down: inicia construindo o nó raiz da ast.
 - recursive descent: vai construindo a ast da maneira que imaginamos ela.
 - operator precedence: TODO.

