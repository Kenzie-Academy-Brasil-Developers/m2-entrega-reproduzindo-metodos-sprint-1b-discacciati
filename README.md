# Entrega: Reproduzindo Métodos de Array e String

O JavaScript fornece vários "métodos de iteração" baseados no mesmo tipo de padrão de callback. Essencialmente, eles são loops prontos, com alguns comportamentos adicionados para ter um pouco de variação do padrão.

Neste exercício, recriei os métodos abaixo, reproduzindo o comportamento desses métodos de Array com suas funções callback, incluindo os parametros opcionais e _sem usar as versões incorporadas do JavaScript_, mostrando como o código é feito por traz do método. 

A intenção é que o meu código obtenha o mesmo resultado que teria utilizando os métodos de iteração. Os métodos reproduzidos são:

1. [forEach()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
3. [map()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
3. [filter()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/filtro) 
4. [find()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
5. [findIndex()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
6. [reduce()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
7. [some()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
8. [every()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
9. [fill()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/fill)
10. [includes()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/contains)
11. [indexOf()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
12. [concat()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
13. [join()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
14. [slice()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
15. [flat()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/flat)
16. [flatMap()](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/flatMap)

As funções são: newForEach, newMap, newFilter, newFind, newFindIndex, newReduce, newSome, newEvery, newFill, newIncludes, newIndexOf, newConcat, newJoin. 

## Por exemplo:

```js
function myCallback(value) {
    return `${value} é muito bom!`
};
let myArr = ["maçã", "uva", "pera"];
let retornoMap = myArr.map(myCallback);
let retornoNewMap = newMap(myArr, myCallback);
retornoMap // Deve retornar ["maçã é muito bom!", "uva é muito bom!", "pera é muito bom!"];
retornoNewMap // Deve retornar ["maçã é muito bom!", "uva é muito bom!", "pera é muito bom!"];
myArr // Deve retornar ["maçã", "uva", "pera"];
```

__Note que possuem o mesmo retorno e o array original não foi modificado, conforme a documentação do Array.prototype.map()__.

