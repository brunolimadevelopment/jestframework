![Imgur](https://i.imgur.com/xhhZ3XJ.png)
![Jest](https://img.shields.io/badge/Jest-323330?style=for-the-badge&logo=Jest&logoColor=white)
![Javascript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)
![Node](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![PopOS](https://img.shields.io/badge/Pop!_OS-48B9C7?style=for-the-badge&logo=Pop!_OS&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)
## Study Repository

Jest is a delightful JavaScript Testing Framework with a focus on simplicity.

It works with projects using: Babel, TypeScript, Node, React, Angular, Vue and more!

------

#### About Class 01

A asserção <b>toBe</b> é usada para verificar se dois valores são estritamente iguais, ou seja, 
se são do mesmo tipo e têm o mesmo valor. 

Essa asserção utiliza o operador de igualdade estrita (=== em JavaScript) para realizar a comparação.

Aqui está um exemplo simples de como você pode usar toBe em um teste Jest:
```
test('exemplo de teste com toBe', () => {
  const resultado = 10 + 5;

  // Verifica se resultado é estritamente igual a 15
  expect(resultado).toBe(15);
});
```
> Neste exemplo, o teste verifica se resultado é estritamente igual a 15 usando expect(resultado).toBe(15). 
Se a asserção falhar, o Jest fornecerá informações sobre a diferença entre os valores esperados e os valores recebidos.

------

#### About Class 02

A asserção <b>toEqual</b> é usada para verificar se dois valores são iguais em termos de conteúdo. 
Essa asserção é frequentemente usada para comparar objetos e arrays de uma maneira mais profunda 
do que a simples igualdade (===).

Quando você usa <b>toEqual</b>, o framework de teste verifica se os valores comparados têm a mesma estrutura 
e contêm os mesmos valores. Se você estiver testando objetos ou arrays, <b>toEqual</b> fará uma comparação profunda dos valores, 
garantindo que cada propriedade ou elemento seja igual.

Aqui está um exemplo usando o framework de teste Jest:

```
test('Exemplo de toEqual', () => {
  const objeto1 = { a: 1, b: 2, c: 3 };
  const objeto2 = { a: 1, b: 2, c: 3 };

  expect(objeto1).toEqual(objeto2);
});
```
Neste exemplo, <b>toEqual</b> é usado para verificar se objeto1 é igual a objeto2. 
A comparação leva em consideração todas as propriedades dos objetos.

Além disso, <b>toEqual</b> é útil para comparar arrays:
```
test('Exemplo de toEqual com arrays', () => {
  const array1 = [1, 2, 3];
  const array2 = [1, 2, 3];

  expect(array1).toEqual(array2);
});
```
Aqui, <b>toEqual</b> garante que os arrays array1 e array2 tenham os mesmos elementos nas mesmas posições.

> Em resumo, a asserção <b>toEqual</b> é usada para verificar igualdade profunda entre dois valores, tornando-se uma escolha apropriada ao lidar com objetos e arrays em testes JavaScript.


------

#### About Class 03

A asserção <b>toBeNull</b> no Jest é usada para verificar se um valor é null. <br/>
Aqui está um exemplo simples:

Suponha que você tenha uma função retornaNull que deve retornar null:

```
// arquivo exemplo.js
function retornaNull() {
  return null;
}

module.exports = retornaNull;
```
Agora, você pode criar um teste usando Jest para garantir que a função realmente retorne null:

```
// arquivo exemplo.test.js
const retornaNull = require('./exemplo');

test('A função retornaNull retorna null', () => {
  expect(retornaNull()).toBeNull();
});

```
Neste exemplo:

    - expect(retornaNull()) é a expressão que representa o valor que você está testando.
    - .toBeNull() é a asserção que verifica se o valor é null.

Se a função retornaNull retornar algo diferente de null, o teste falhará, indicando que a função não está se comportando conforme o esperado.

> Lembre-se de que o Jest fornece várias outras asserções úteis para testar diferentes condições. toBeNull é específico para verificar se um valor é null.