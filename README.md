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
      

 
## Diferenças entre fuunções e métodos
 
Here are the technologies used in this project.
 
* Ruby version  x.x.x
* Rails version x.x.x
* ...
 
 
## Diferenças entre Arrays e Objetos
 
* Github
* ...
 
