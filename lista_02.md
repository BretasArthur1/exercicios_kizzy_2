# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.

Resposta: Letra B. Pois em uma condicao com o comparativo or e uma expressao que temos falso ou verdadeiro, temos o resultado verdadeiro como resposta. E ele imprime o valor da soma dos numeros de 1 a 5.
______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

Resposta: Letra D. Pois mesmo com um codigo tendo um loop com pos condicao e outro com pre condicao ambos vao executar o codigo ao menos uma vez. reduzindo o saldo para -100. O unico adendo seria que o segundo codigo, seria mais eficiente pois a pre condicao impede que o codigo rode uma vez desncessaria. Apesar dessa vez "a mais" que o primeiro roda, ele nao chega a atualizar a variavel saldo, pois ela esta fora do loop.
______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".

Resposta: Letra D. A descrição mais precisa seria a letra D pois, ela exprime exatamente passo a passo o que o código faz.

______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.


D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

Resposta: Letra D.
______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

B) Preload -> Create -> Update

C) Load -> Initialize -> Render

D) Begin -> Play -> End

Letra B.
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

Letra B.
______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

recebe idade

se (idade < 16)
    exibe "não pode votar!" 
        senao se (idade >= 16 e idade < 18)
            exibe "voto facultativo!"
                senao
                    exibe "voto obrigatorio!" 
______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

Classe derivada Retangulo de FormaGeometrica
        Atributos:
            -Base 
            -Altura
            
            Método Construtor(cor):
                super(cor)

            Metodo CalcularArea():
                AreaRetangulo = Lado x Altura
                retorna AreaRetangulo
            
Classe derivada Circulo de FormaGeometrica
        Atributos:
            -Raio
            -Pi = 3,14159

            Método Construtor(cor):
                super(cor)

            Metodo CalcularArea():
                AreaCirculo = Pi x r^2
                retorna AreaCirculo            

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

Considere a fórumla de atualização velocidade:
```
    velocidade = velocidadeInicial + aceleracao*tempo
```

Classe SimuladorDeCorrida:
    Atributos:
        - velocidadeInicial
        - aceleracao
        - velocidadeMaxima
        - tempoMaximo
        - distanciaCorrida

    Método Construtor(velocidadeInicial, aceleracao, velocidadeMaxima, tempoMaximo, distanciaCorrida):
        

    Método SimularCorrida():
        tempo = 0
        distanciaPercorrida = 0
        velocidade = velocidadeInicial

        Enquanto distanciaPercorrida < distanciaCorrida E tempo < tempoMaximo:
            Se velocidade < velocidadeMaxima:
                velocidade = velocidadeInicial + aceleracao * tempo
            Senão:
                velocidade = velocidadeMaxima

            distanciaPercorrida += velocidade / 60  // Converte velocidade por hora em distância por minuto
            tempo += 1  // Incrementa o tempo em minutos

            Se velocidade > velocidadeMaxima:
                velocidade = velocidadeMaxima  // Limita a velocidade à máxima permitida

        Se distanciaPercorrida >= distanciaCorrida:
            Retorna "O carro completou a corrida em " + tempo + " minutos."
        Senão:
            Retorna "O carro não completou a corrida dentro do tempo máximo."




______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função SomaDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."
    Senão:
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0]) # Considerando que todas as linhas têm o mesmo número de colunas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a soma
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizSoma <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Soma das matrizes:")
ImprimirMatriz(matrizSoma)

Resposta: 

Função MultiplicaMatrizes(matrizA, matrizB):
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. O número de colunas da matriz A deve ser igual ao número de linhas da matriz B."

    linhasA <- tamanho(matrizA)
    colunasA <- tamanho(matrizA[0])
    linhasB <- tamanho(matrizB)
    colunasB <- tamanho(matrizB[0])
    matrizResultado <- novaMatriz(linhasA, colunasB)

    # Loop para percorrer as linhas da matriz A
    Para i de 0 até linhasA-1 faça:
        # Loop para percorrer as colunas da matriz B
        Para j de 0 até colunasB-1 faça:
            # Inicializa o elemento da matriz resultado com 0
            matrizResultado[i][j] <- 0
            # Loop para calcular o produto dos elementos e somá-los ao elemento da matriz resultado
            Para k de 0 até colunasA-1 faça:
                matrizResultado[i][j] <- matrizResultado[i][j] + (matrizA[i][k] * matrizB[k][j])

    Retornar matrizResultado

