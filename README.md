# BANCO DIGITAL
## Programação básica JS

Em JavaScript as variáveis sáo "içadas", também conhecido como hoisting, até o topo de execução. Esse mecanismo movimenta as variáveis para o topo do seu escopo antes da execução do código, ou seja, podemos utilizar as variáveis mesmo antes de terem sido declarada.

Ex.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script type="text/javascript">
        var exibeMensagem = function() { 
            mensagem = 'Olá Mundo!'; 
            console.log(mensagem); 
            var mensagem;
        }
        exibeMensagem();   
    </script>
    <title>Exercicio 4</title>
</head>
<body>
</body>
</html>
```
Se analisar o console do navegador, verá que será impresso Olá Mundo!

Ao utilizar uma variável informamos uma palavra-chave para esclarecer ao JavaScript que estamos utilizando uma variável, hoje são utilizadas as três palavras-chave VAR, LET e CONST.

## Diferenças entre let, var, const
 
* var
Utilizando o conceito de hoisting a variável quando utiliza da palavra-chave var, inicializa automaticamente como undefined(indefinido), caso não seja atribuido um outro valor.
Pensando em um sistema com várias linhas de código, o controle dessa variáveis se tornaria muito trabalhoso, até mesmo para programadores experientes.

* let
Pensando em solucionar o problema do escopo de bloco, a ECMAScript 6 destinou-se a disponibilizar uma ferramenta e foi criada a palavra-chave let, que se restringe apenas ao escopo do bloco de instrução, não permitindo que essa variável seja utilizada fora deste escopo.

      Ex.
      
      <!DOCTYPE html>
      <html lang="en">
      <head>
          <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <script type="text/javascript">
              var exibeMensagem = function() {
              if(true) { 
                  var escopoFuncao = 'Escopo Função'; 
                  let escopoBloco = 'Escopo Bloco';
                  console.log(escopoBloco);  
              } 
              console.log(escopoFuncao);  
              console.log(escopoBloco); 
              }       
              exibeMensagem();
          </script>
          <title>Exercicio 4</title>
      </head>
      <body>
      </body>
      </html>
      
No código acima, note que será impresso Escopo Bloco, se sequencia Escopo Função e em seguida será apresentado um erro. Isso acontece por conta da variável escopoBloco ser restrita a apenas o bloco de instruções.

* const
Abreviação de constante, onde o valor informado é fixo, pois o comportamento fundamental de uma constante é que uma vez atribuído um valor a ela, este não pode ser alterado.
 
## Diferenças entre funções e métodos
 
| FUNÇÃO                                                                         	| MÉTODO                                                                                                                                                     	|
|--------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------------	|
| Uma função pode ser chamada diretamente por seu nome.                          	| Um método consiste em um código que pode ser chamado pelo nome de seu objeto <br>e seu nome de método usando a notação de ponto ou a notação de colchetes. 	|
| Uma função pode passar os dados que são operados e pode <br>retornar os dados. 	| O método opera os dados contidos em uma classe.                                                                                                            	|
| Os dados passados para uma função são explícitos.                              	| Um método passa implicitamente o objeto no qual foi chamado.                                                                                               	|
| Uma função vive sozinha.                                                       	| Um método é uma função associada a uma propriedade do objeto.                                                                                              	|
 
 
## Diferenças entre Arrays e Objetos

Basicamente ambos em JavaScript são objetos, os objetos simples não tem "propriedades", então existem diversos tipos de objetos que estendem o objeto simples, o Array por si só é um objeto estendido, até mesmo strings são objetos em JavaScript.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script type="text/javascript">
        let x = [];
        let y = {};
        let a = new Array;
        let b = new Object; 
        console.log(x instanceof Array);  
        console.log(y instanceof Array); 
        console.log(a instanceof Array); 
        console.log(b instanceof Array); 
    </script>
    <title>Exercicio 4</title>
</head>
<body>
</body>
</html>
```


