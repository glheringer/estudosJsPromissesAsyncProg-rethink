# Curso sobre JavaScript Promises e Async Programming da Pluralsight.
## Arrow Functions
As arrows functions são uma outra sintaxe para escrita de funções, mais curta e objetiva, o nome decorre do simbolo => (arrow, ou flecha) contido em sua sintaxe.
- Principais formas de escrita: 
  ``` bash
   
  //com argumentos
  (a,b) => {
    return a + b;
  }

  (a,b) => a + b; 
  
  
  let a = 5;
  let b = 10;

  let c = (num1,num2) => a + b;

  // ou 

  let c = (num1,num2) => {
      return a + b;
  }

  // um argumento
  let frase =  `Hello World`;

  let fraseArray = (frase) => frase.split(' ');
  console.log(fraseArray(frase)); //chamando a funçao criada
 
  ```
## Promises
Estudos de JavaScript Promises(promise.js) and Async Programming(await.js)

Callback Pyramid of Doom: Um problema comum que surge qunado o programador usa muitos leveis hierárquica para acessar uma função (codigo sujo e de difícil reparo), por mais que uma função  assíncrona  esteja entre o código ela só será  chamada (callback) no final do processamento .

## Como promises ajudam ?

Promise é um object que representa um eventual complemento ou falha de uma operação  assíncrona  e de seu valor resultante.

States:

- Pending (quando o promise ainda está processando);
- Fulfilled (quando o promise completou com sucesso, retorna um unico valor);
- Rejected (retorna o porque foi rejeitado);
- Settled or Resolved(esta em Fulfiller ou Rejected, não esta mais pendente);

```JavaScript 
const readFile = file => new Promise((resolve, reject) =>{
  fs read file(file, (err, contents) => {
  if (err){
    reject(err)
  } else{
    resolve(contents)
  }
 })
})
readFile('./in1.txt')
  .then(contents => {
  console.log(String(contents))
  return readFile('./in2.txt')
  })
  .then(contents => {
    console.log(String(contents))
  })
```
O promisse alarga o codigo para baixo e nao para o lado formando uma pirâmide assim facilitando manutenção 
Comsumo de API:

Objetos primordiais:
- Addresses;
- Items 
- Orders 
- Users 
- Items Categories 
- Order Statuses


## Async/await

Uma função  async é uma promisse que pode ser gerada em um formato diferente, possibilitando  dar um await na promisse então  facilita a manipulação  assíncrona.
```JavaScript 
const init = async() => {
  try{
  const contents = await readFile('./in1.txt')
  const contents2 = await readFile('./in2.txt')
  console.log(String(contents))
  console.log(String(contents2))
  }catch(err){
    console.log(err)
  }
}  
```
