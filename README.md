# Estruturas de Controle em JavaScript

Este repositório documenta a pesquisa e os exemplos práticos desenvolvidos para as seguintes estruturas de controle em JavaScript:

- If, else if, e else
- Switch case
- For loop
- While loop

## Integrantes do Grupo
- Carlos Eduardo Mocinho Da Silva
- Eduarda De Barros Cicatto

## If, Else If, e Else

### Características Principais
- `if`: Usado para executar um bloco de código se uma condição especificada for verdadeira.
- `else if`: Permite a definição de uma nova condição se a condição anterior for falsa.
- `else`: Executa um bloco de código se todas as condições anteriores forem falsas.

### Quando Usar
Utilize quando precisar executar diferentes blocos de código com base em várias condições.

### Exemplos Práticos

### exemplos If e Else
```javascript

// Exemplo 1: Verificação de aprovação de aluno
function verificarAprovacao(nota) {
    if (nota >= 7) {
        console.log("Aprovado!");
    } else {
        console.log("Reprovado. Estude mais um pouco.");
    }
}

verificarAprovacao(8.5); // Saída: Aprovado!
verificarAprovacao(6); // Saída: Reprovado. Estude mais um pouco.

// Exemplo 2: Desconto em uma loja com base no valor da compra
function calcularDesconto(valorCompra) {
    if (valorCompra > 500) {
        console.log("Desconto de 20% aplicado!");
        return valorCompra * 0.8;
    } else {
        console.log("Desconto de 10% aplicado!");
        return valorCompra * 0.9;
    }
}

console.log(calcularDesconto(750)); // Saída: Desconto de 20% aplicado! Valor final: 600
console.log(calcularDesconto(450)); // Saída: Desconto de 10% aplicado! Valor final: 405

```
## Fim dos Exemplos

Nos exemplos fornecidos, a estrutura if e else é utilizada para criar decisões lógicas dentro do código. No Exemplo 1, a estrutura é usada para determinar se um aluno está aprovado ou reprovado com base em sua nota. A condição if (nota >= 7) verifica se a nota é maior ou igual a 7, o que indica aprovação. Caso contrário, o bloco else é executado, indicando reprovação. No Exemplo 2, a estrutura decide qual percentual de desconto aplicar em uma compra. Se o valor da compra for maior que 500, um desconto maior é aplicado; se não, um desconto menor é concedido. Ambos os exemplos demonstram como if e else podem ser usados para controlar o fluxo do programa e tomar decisões baseadas em condições específicas, tornando o código mais dinâmico e adaptável a diferentes situações.

## Exemplos Uso do Switch Case

```javascript
// Exemplo 1: Resposta automática baseada no dia da semana
function respostaDiaDaSemana(dia) {
    switch (dia) {
        case 'segunda':
            console.log("Começando a semana com energia!");
            break;
        case 'terça':
            console.log("Segundo dia, ainda com força total!");
            break;
        case 'quarta':
            console.log("Metade da semana, já estamos lá!");
            break;
        case 'quinta':
            console.log("Quase sexta, aguente firme!");
            break;
        case 'sexta':
            console.log("Finalmente sexta, bom fim de semana!");
            break;
        default:
            console.log("Aproveite o fim de semana!");
            break;
    }
}

respostaDiaDaSemana('segunda'); // Saída: Começando a semana com energia!
respostaDiaDaSemana('sábado');  // Saída: Aproveite o fim de semana!

// Exemplo 2: Cálculo do preço final com base no tipo de produto
function calcularPreco(tipoProduto, precoBase) {
    switch (tipoProduto) {
        case 'eletronico':
            return precoBase + (precoBase * 0.20); // Acréscimo de 20%
        case 'vestuario':
            return precoBase + (precoBase * 0.10); // Acréscimo de 10%
        case 'alimento':
            return precoBase; // Sem acréscimo
        default:
            console.log("Tipo de produto não reconhecido.");
            return precoBase;
    }
}

console.log(calcularPreco('eletronico', 1000)); // Saída: 1200
console.log(calcularPreco('livro', 50));        // Saída: Tipo de produto não reconhecido. 50
```
## Fim dos Exemplos

Nos exemplos acima, utilizamos a estrutura `switch case` para tomar decisões com base em um valor específico de uma variável. 

No **Exemplo 1**, a função `respostaDiaDaSemana` recebe um dia da semana como argumento e utiliza o `switch case` para imprimir uma mensagem correspondente a esse dia. Cada `case` representa um dia da semana e executa um `console.log` com uma mensagem específica. O `break` é importante para sair do `switch` após a execução do caso correspondente, evitando que os casos subsequentes sejam também executados. O `default` é usado como uma condição de captura para todos os valores que não correspondem a nenhum dos `cases` definidos.

No **Exemplo 2**, a função `calcularPreco` determina o preço final de um produto com base em seu tipo. Aqui, o `switch case` é usado para aplicar diferentes taxas de acréscimo ao preço base, dependendo do tipo de produto. Se o tipo de produto não for reconhecido, uma mensagem é impressa e o preço base é retornado sem acréscimos.

Esses exemplos demonstram a eficácia do `switch case` em substituir múltiplas estruturas `if else` quando temos um único valor a ser comparado contra várias possibilidades, tornando o código mais limpo e fácil de entender.


## Exemplos Uso do For Loop

```javascript
// Exemplo 1: Iteração sobre um array de números
const numeros = [1, 2, 3, 4, 5];
for (let i = 0; i < numeros.length; i++) {
    console.log(numeros[i]);
}

// Exemplo 2: Contagem regressiva
for (let contador = 10; contador > 0; contador--) {
    console.log(contador);
}
console.log("Feliz ano novo!");
```
## Fim dos Exemplos

Nos exemplos fornecidos, a estrutura de loop `for` é utilizada para executar um bloco de código repetidamente por um número definido de vezes.

No **Exemplo 1**, temos um array chamado `numeros` que contém cinco elementos. O loop `for` é usado para iterar sobre cada elemento do array. A variável `i` é inicializada com 0 e, enquanto `i` for menor que o comprimento do array (`numeros.length`), o loop continuará a executar, incrementando `i` a cada iteração. Dentro do loop, `console.log(numeros[i])` imprime o elemento atual do array.

No **Exemplo 2**, o loop `for` é configurado para criar uma contagem regressiva. A variável `contador` é inicializada com 10 e, enquanto `contador` for maior que 0, o loop continuará a executar, decrementando `contador` a cada iteração. Após o loop terminar, a mensagem "Feliz ano novo!" é impressa, simulando uma contagem regressiva para o ano novo.

O loop `for` é uma ferramenta poderosa em JavaScript que permite não apenas iterar sobre arrays, mas também executar qualquer tipo de operação repetitiva de forma controlada e previsível. É uma das estruturas de controle mais comuns e úteis na programação.

## Exemplos Uso do While

```javascript
// Exemplo 1: Executar um bloco de código pelo menos uma vez e repetir enquanto a condição for verdadeira
let contador = 0;
do {
    console.log(contador);
    contador++;
} while (contador < 5);

// Exemplo 2: Solicitar ao usuário para inserir um número até que o número seja maior que 10
let numero;
do {
    numero = prompt("Insira um número maior que 10:");
} while (numero <= 10);
```
## Fim dos Exemplos

Nos exemplos acima, utilizamos a estrutura de loop `do while` para executar um bloco de código enquanto uma condição especificada é verdadeira, com a garantia de que o bloco será executado pelo menos uma vez.

No **Exemplo 1**, inicializamos a variável `contador` com 0. O bloco de código dentro do `do` será executado primeiro, sem verificar a condição. Após a execução do bloco, a condição `while (contador < 5)` é avaliada. Se for verdadeira, o bloco é executado novamente. Esse processo se repete até que a condição se torne falsa. Neste caso, o console imprimirá os números de 0 a 4.

No **Exemplo 2**, o loop `do while` é usado para solicitar ao usuário que insira um número repetidamente até que ele insira um número maior que 10. A função `prompt` é usada para coletar a entrada do usuário. Após cada entrada, a condição `while (numero <= 10)` é verificada. Se o número inserido for menor ou igual a 10, o prompt será exibido novamente. Este exemplo é teórico, pois `prompt` é uma função que só funciona em navegadores e não em ambientes de execução de scripts como Node.js.

O loop `do while` é particularmente útil quando você precisa garantir que um bloco de código seja executado pelo menos uma vez, independentemente da condição, antes de verificar se a condição para continuar o loop é verdadeira. É uma estrutura de controle que oferece uma lógica de repetição com uma verificação de condição no final do loop.

## Fim do README
