# Trabalho-TVD
Explicação de codigo de Técnicas de Desenvolvimento de Vídeojogos
Feito por:   
João Costa nº27931  
Rafael Santos nº27930  
Afonso Paiva nº27915  
*** 
# Classes do projeto:

 O projeto e dividido em 6 classes nomeadamente:

## Bola.cs
 A classe bola.cs faz toda a lógica do movimento e comportamento da bola, tendo a classe objetos como pai.
### Variaveis

As variaveis declaradas nesta classe são:  
* Velocity: Que vai determinar a velocidade da bola.  
* Random: Que chama a classe random para gerar um valor aleatorio.  

### Métodos  

   `Launch`  O metodo launch inicia a bola com uma velocidade predeterminada, calcula um angulos aleatorio  para lancar a bola, define a posição da bola no centro do ecrã e calcula a velocidade da bola consoante o angulo.  
   `CheckWallCollision`  Trata de checkar se a bola colide com as paredes, tambem reproduz um som consoante a bola bater no topo ou em baixo.  
   `Move`  Chama pela classe objetos, e movimenta a bola caso ela tenha colidido.

### Construtor

O contrutor so inicia um objeto da classe Random.


### Método Launch  

* Inicia o movimento da bola com uma determinada velocidade.  
* Calcula um ângulo aleatório para lançar a bola.  
* Define a posição inicial da bola no centro da tela. 
* Calcula a velocidade da bola com base no ângulo e em uma direção aleatória.  
### Método CheckWallCollision
* Verifica e trata as colisões da bola com as paredes da tela.  
* Se a bola atinge o topo ou o fundo da tela, inverte sua velocidade na direção Y e reproduz um som.  

### Método Move:
* Sobrescreve o método Move da classe pai (Objetos).
* Move a bola com base no vetor de movimento fornecido.
* Após o movimento, verifica se houve colisão com as paredes chamando o método CheckWallCollision.




