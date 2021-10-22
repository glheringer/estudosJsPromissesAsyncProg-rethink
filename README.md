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
