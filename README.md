# teste_econdo
faça um algorítmo para retornar strings duplicadas e o valor
//Solução em js

//+>Dada uma palavra qualquer;
//=>escreva as letras repetidas;
//=>e a quantidade de repetições;
//___________________________________________________
//var countChars = function (word) {
//  console.log(word);
//}
//countChars('Programming');
//___________________________________________________

function frequency(text) {

  const map = new Map();
 
  for (let letter of text) {
    let count = map.get(letter) || 0;    
    map.set(letter, count+1);
  }
 
  return map;
}

const frequencies = frequency("Programming");

for (let [letter, total] of frequencies) {
  console.log(`${letter} => ${total}`);
}
