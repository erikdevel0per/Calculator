
# Calculadora em Java (Sem Interface)

## Descrição
Simples Calculadora feita em Java (Sem Interface Interativa)

## Estrutura e Componentes:
Importações:

- `java.util.InputMismatchException`: Utilizada para capturar exceções de entrada inválida, ou seja, quando o usuário insere um valor que não pode ser convertido para o tipo esperado (neste caso, `Double`).
- `java.util.Locale`: Usada para garantir que a comparação de strings (para "S" ou "N") seja feita de maneira insensível ao caso (maiúsculas ou minúsculas).
- `java.util.Scanner`: Usado para ler a entrada do usuário.

Variáveis:

- `valorUm`: Armazena o primeiro valor inserido pelo usuário, do tipo `Double`.
- `valorDois`: Armazena o segundo valor inserido pelo usuário, também do tipo `Double`.
- `operacao`: Armazena a operação matemática escolhida pelo usuário (como `+`, `-`, `*`, `/`).
- `continuar`: Um valor booleano que controla o loop, permitindo que o programa continue solicitando novas operações enquanto o usuário desejar.

Bloco Principal (`main`):

- O programa começa criando um objeto `Scanner` para ler a entrada do usuário.
- Em seguida, entra em um `do-while` loop, onde o usuário pode realizar cálculos sucessivos até que escolha parar.
- O bloco `try-catch` é utilizado para capturar exceções do tipo `InputMismatchException`, caso o usuário insira um valor inválido (não numérico) ao tentar realizar os cálculos.
- O programa solicita três entradas: `valorUm`, a operação, e `valorDois`, e então exibe o resultado calculado pela função `realizarCalculo`.

Método `verificarNovaOperacao`:

- Este método pergunta ao usuário se ele deseja realizar uma nova operação.
- O método utiliza `Scanner` para capturar a resposta do usuário e converte a resposta para maiúsculas para garantir que a comparação seja insensível a maiúsculas/minúsculas.
- Se o usuário digitar "N", o método retorna `false`, indicando que o programa deve parar. Se o usuário digitar qualquer outra coisa, o método retorna `true`, permitindo que o programa continue.

Método `realizarCalculo`:

- Este método é responsável por realizar o cálculo real, com base na operação fornecida pelo usuário.
- Ele usa uma estrutura `switch` para escolher a operação correta (`+`, `-`, `*`, `/`), e executa o cálculo com os dois valores fornecidos.
- Se a operação fornecida for inválida (não uma das opções listadas), o programa exibe uma mensagem informando que a operação é inválida.

##Exceções e Erros:

- `InputMismatchException`: Esse bloco `catch` lida com o erro quando o usuário fornece entradas que não podem ser convertidas para um número (`Double`). Por exemplo, se o usuário digitar uma string como "abc" em vez de um número.
- Divisão por zero: O código não lida explicitamente com erros de divisão por zero. Se o usuário inserir `0` como o segundo valor e escolher a operação de divisão (`/`), o programa lançará uma exceção `ArithmeticException` devido à tentativa de divisão por zero.

## Fluxo de Execução:

- O programa solicita os valores e a operação.
- Ele realiza o cálculo usando o método `realizarCalculo`.
- Exibe o resultado e pergunta se o usuário deseja realizar outra operação.
- O processo continua até que o usuário decida parar (digitando "N").

## Melhorias Possíveis:
- Tratamento de divisão por zero: O programa poderia verificar se o segundo valor é zero antes de tentar dividir, e se for o caso, exibir uma mensagem de erro apropriada, evitando a exceção.
- Fechamento do scanner: O scanner é criado dentro do `main` e também no método `verificarNovaOperacao`, o que pode gerar problemas se for fechado múltiplas vezes. Seria melhor ter um único objeto `Scanner` para evitar esse problema.
Se uma exceção ocorrer (como um valor não numérico), o programa informa o erro e termina.

## Conclusão:

Esse código implementa uma calculadora simples, com a capacidade de realizar múltiplas operações em uma única execução, tratando exceções de entrada de dados de forma básica. O código é funcional, mas pode ser melhorado no tratamento de exceções e na estrutura de objetos


## **Muito Obrigado pela sua atenção!**
