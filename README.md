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

 &nbsp;&nbsp;&nbsp;&nbsp;**`Velocity`** Que vai determinar a velocidade da bola.
  
 &nbsp;&nbsp;&nbsp;&nbsp;**`Random`** Que chama a classe random para gerar um valor aleatorio.  

### Métodos  

&nbsp;&nbsp;&nbsp;&nbsp;**`Launch`**  O metodo launch inicia a bola com uma velocidade predeterminada, calcula um angulos aleatorio  para lancar a bola, define a posição da bola no centro do ecrã e calcula a velocidade da bola consoante o angulo.
     
&nbsp;&nbsp;&nbsp;&nbsp;**`CheckWallCollision`**  Trata de checkar se a bola colide com as paredes, tambem reproduz um som consoante a bola bater no topo ou em baixo.
     
&nbsp;&nbsp;&nbsp;&nbsp;**`Move`**  Chama pela classe objetos, e movimenta a bola caso ela tenha colidido.

### Construtor

&nbsp;&nbsp;&nbsp;&nbsp;O contrutor so inicia um objeto da classe Random.    

> No fundo o código gere o funcionamento e comportamento da bola, também inclui o lançamento inicial e as colisões existentes. 

<br>
</br>

## Input.cs
A classe Input.cs recebe a a entrada do jogador  

### Variáveis

&nbsp;&nbsp;&nbsp;&nbsp;**`TecladoTecla`** Verifica se a tecla foi pressionada pelo utilizador.

### Métodos 


### Construtor





<br>
</br>
## Jogador.cs




<br>
</br>
## Som.cs




<br>
</br>
## Game1.cs






