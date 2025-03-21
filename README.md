# Ponderada-Semana-6

# Questões objetivas
## 1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

## Resposta - 1
**a) A saída será undefined seguido de erro**

Justificativa:

 A variável x é declarada por um “var” que é, quando o código escrito em java script é ativado eleva essa variável para ser lida, entretanto, não é efetuado o mesmo com relação ao valor. Assim, a variável x não atribui a ela nenhum valor, resultando em um “undefined”.
 A variável y foi declarada por “let” o que faz com que ela não seja “elevada” e tratada como variável antes da leitura do “console.log(y)”, dessa maneira, por não ser identificada nenhuma variável ele segue como um erro por não haver nada sendo declarado.
 _____

## 2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

## Resposta - 2
**b) Substituir if (a || b === 0) por if (a === 0 && b === 0)**

Justificativa:

 A alternativa que responde de forma mais adqueda a questão seria a letra b). Visto que, dessa maneira apenas quando calculamos a soma de 0 + 0 teria esse resultado de "Erro: número inválido", assim, mesmo se a soma ocorrer com um dos argumentos dessa função seja 0.
______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

## Resposta - 3
**b) O código imprime 200.**

Justificativa:

 Isso ocorre devido a falta de um break na case "eletrônico", pois assim o comando lê até achar um break, que ocorre na case seguinte, "vestuário".
______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

## Resposta - 4
**d) 24**

Justificativa:

 Esse é o resultado pois, ao utilizar o ".map" ele multiplica todos os números da lista por 2, resultando em um array [2, 4, 6, 8, 10]. Em seguida, com o ".filter", ele mantem apenas os resultados maiores que 5, dessa forma cria o seguinte array: [6, 8, 10]. Dessa forma, o ".reduce" executa uma soma dos valores que ali permaneceram, assim, resultando no calculo: 6 + 8 + 10 = 24.
 
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

## Resposta - 5
**c) ["banana", "abacaxi", "manga", "laranja"]**

Justificativa:

 Após o array ser declarado, o método "splice" adiciona ou remove elementos desse array. No caso deste código, esse método está adicionando elementos, no qual o primeiro digíto, no caso "1" diz a partir de qual índice os novos elementos entraram, e o segundo, no caso "2", a quantidade de elementos já existemtes no array que serão substituidos. Acarretando na resposta.
 
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

## Resposta - 6
**a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.**

Justificativa:

 A segunda afirmativa explica a primeira quando, explica sobre o uso da palavra "extends". Dessa forma deixa claro como funciona a herança das classes e como não há necessidade de repetir os metodos abordados na classe anterior, ou classe mãe para classe filha.
 
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

## Resposta - 7
**a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.**

Justificativa:

 As afirmações I e II são verdadeiras porque Funcionario herda de Pessoa e pode acessar nome e idade, além de sobrepor o método apresentar() chamando super.apresentar(). A afirmação III é falsa, pois JavaScript suporta herança de classes com class e extends.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

## Resposta - 8
**b) A asserção é verdadeira e a razão é falsa.**

Justificativa:

 Em relação ao polimorfismo apresentado na "asserção" está correto, entretanto quanto a razão está incorreta, pois no JavaScript o polimorfismo é executado por via da herança e sobrescrita por métodos.
______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
## Resposta - 9

```javascript
// Crie uma função que receba um array de números 
// e retorne a soma de todos os elementos desse array multiplicados por 2. 
function somaArray(numeros) {

  // escreva seu código aqui
  var soma = 0;

  // Criando o for
    for (i = 0; i < numeros.length; i++) {

      // O valor atribuido a variavel soma é atualizado e usado para somar com o valor do array multiplicado por 2,
      //até que o mesmo se chegue ao final do array.
        soma = soma + 2*numeros[i];
    }
    
    // Retornando o valor da variavel soma.
    return soma;
}

console.log(somaArray([1, 2, 3, 4,]));
```

______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

## Resposta - 10

```javascript
// Classe Produto com atributos nome e preco
class Produto {
  constructor(nome, preco) { 
    this.nome = nome;
    this.preco = preco;
  }

  // Método calcularDesconto() com desconto fixo de 10%
  calcularDesconto() {
    return this.preco * 0.1;
  }
}

// Classe Livro que herda de Produto e modifica calcularDesconto()
class Livro extends Produto {
  constructor(nome, preco, autor) {
    super(nome, preco);
    this.autor = autor;
  }

  // Método calcularDesconto() com desconto de 20%
  calcularDesconto() {
    return this.preco * 0.2;
  }
}

// Criando um livro
const livro = new Livro("Clean Code", 150, "Robert C. Martin");
console.log(`Livro: ${livro.nome}`);
console.log(`Autor: ${livro.autor}`);
console.log(`Preço original: R$ ${livro.preco}`);
console.log(`Preço final: R$ ${livro.preco - livro.calcularDesconto()}`);

```
Herança é um mecanismo em que uma subclasse, no caso a classe "Livro",  herda atributos e métodos de outra superclasse, nesse caso case classe "Produto". Neste exemplo, a classe Livro herda da classe Produto. A subclasse Livro pode acessar e usar os atributos e métodos da superclasse Produto, e também pode modificar esses métodos, como fizemos com calcularDesconto().
