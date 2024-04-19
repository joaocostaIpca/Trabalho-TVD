# Trabalho-TVD
Explicação de codigo de Técnicas de Desenvolvimento de Vídeojogos
<br>
</br>

Feito por:   
* João Costa nº27931 
* Rafael Santos nº27930  
* Afonso Paiva nº27915  
*** 

# Índice
1. [ Classes do Projeto ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#1-classes-do-projeto)  
   1.1 [ Bola.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#11-bolacs)  
   1.2 [ Input.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#12-inputcs)  
   1.3 [ Jogador.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#13-jogadorcs)  
   1.4 [ Som.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#15-objetoscs)  
   1.5 [ Objetos.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#15-objetoscs) 
2. [ Game1.cs ](https://github.com/joaocostaIpca/Trabalho-TVD/tree/main?tab=readme-ov-file#15-objetoscs)



## 1. Classes do Projeto

 O projeto e dividido em 6 classes nomeadamente:

## 1.1. Bola.cs
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

## 1.2. Input.cs
A classe Input.cs recebe a a entrada do jogador  

### Variáveis

&nbsp;&nbsp;&nbsp;&nbsp;**`Direction`** Vetor bidimensional (Vector2) que armazena a direção do movimento.

&nbsp;&nbsp;&nbsp;&nbsp;**`keyboardState`** Representa o estado atual do teclado.

&nbsp;&nbsp;&nbsp;&nbsp;**`PlayerIndex`** Parâmetro de uma função que especifica qual o jogador em causa para o qual estamos e verificamos a entrada do teclado.

### Métodos 

&nbsp;&nbsp;&nbsp;&nbsp;**`TecladoTecla`** Verifica se a tecla foi pressionada pelo utilizador.

> Nota que nos encontramos perante um método estático que basicamente se encarrega da entrada de cada utilizador para tornar possível o movimento das barras.
<br>
</br>

## 1.3. Jogador.cs
A classe Jogador.cs implementa um método de movimento específico para controlar a posição de um jogador.

### Variaveis

 &nbsp;&nbsp;&nbsp;&nbsp;**`pontuacao`** Este inteiro guarda a pontuação do jogador
  
 &nbsp;&nbsp;&nbsp;&nbsp;**`Posicao`** Indica a posição do jogador

 &nbsp;&nbsp;&nbsp;&nbsp;**`Textura`**  Um objeto da classe (Texture2D) refere-se a textura do jogador na tela.

  &nbsp;&nbsp;&nbsp;&nbsp;**`movimento`**  Vetor bidimensional que indica o movimento do player


### Métodos  

&nbsp;&nbsp;&nbsp;&nbsp;**`Move`**  Isto é um método publico que verifica se o jogador ultrapassou os limites da tela, se esse não for o caso irá executar o movimento do jogador

> Esta classe basicamente controla a pontuação e o movimento do jogador, incluindo um limitador, para este não sair da tela.
     
<br>
</br>


## 1.4 Som.cs
Esta classe armazena e executa os efeitos sonoros do jogo.

### Variaveis


 &nbsp;&nbsp;&nbsp;&nbsp;**`SomBarra`** Controla o som que é efetuado pela barra.

 &nbsp;&nbsp;&nbsp;&nbsp;**`SomBola`** Controla o som que é efetuado pela bola.

### Métodos  

&nbsp;&nbsp;&nbsp;&nbsp;**`CarregarSom`** Este método utiliza o (Content Manager) para atribuir os efeitos sonoros da bola e da barra.

> Nota que o (SoundEffect) é uma classe fornecida pela XNA Framework para o uso de efeitos sonoros.

<br>
</br>


## 1.5 Objetos.cs
Esta classe regista os objetos existentes.

### Variaveis


 &nbsp;&nbsp;&nbsp;&nbsp;**`Posicao`** Representa a posição do objeto

 &nbsp;&nbsp;&nbsp;&nbsp;**`Textura`** É a textura do objeto, do tipo Texture2D da framework


### Métodos  

&nbsp;&nbsp;&nbsp;&nbsp;**`Draw`**  Isto desenha o objeto na tela com o (SpriteBatch), através da (Textura) e a (Posicao) .

&nbsp;&nbsp;&nbsp;&nbsp;**`Move`** Ele recebe o (movimento) e a (Posicao) do objeto e soma esse vetor à posição atual.


&nbsp;&nbsp;&nbsp;&nbsp;**`Bounds`** Retângulo que delimita as bordas do jogo e que representa a área ocupada pelo objeto. É utilizado para detetar colisões. 


> Observa-se que esta classe foca-se principalmente na decção de colisões para o jogo.

<br>
</br>

***

## 2. Game1.cs

Esta classe é a principal do programa.

### Variaveis


 &nbsp;&nbsp;&nbsp;&nbsp;**`Posicao_barra`** Representa a posição da Barra

 &nbsp;&nbsp;&nbsp;&nbsp;**`velocidade_bola`** Representa a velocidade da bola 

 &nbsp;&nbsp;&nbsp;&nbsp;**`Teclado_velocidade_barra`** Representa a o fator de multiplicacao para a velocidade da bola

 &nbsp;&nbsp;&nbsp;&nbsp;**`Placar_maximo`** Representa o valor maximo do placar

 &nbsp;&nbsp;&nbsp;&nbsp;**`framerate`** Representa uma constante para defenir a framerate

 &nbsp;&nbsp;&nbsp;&nbsp;**`graphics`** é uma variavel que faz com que basicamente funcione o programa graficamente  

 &nbsp;&nbsp;&nbsp;&nbsp;**`spritebatch`** Permite nos desenhar as texturas que nos pretendemos dentro do jogo

 &nbsp;&nbsp;&nbsp;&nbsp;**`altura e largura`** Representa a altura e largura do tamanho da janela

 &nbsp;&nbsp;&nbsp;&nbsp;**`jogador1 e jogador2`** Sao variaveis tipos objetos que herdam tudo da classe jogador

 &nbsp;&nbsp;&nbsp;&nbsp;**`Bola`** É uma variavel do tipo objeto que herda a classe bola 

 &nbsp;&nbsp;&nbsp;&nbsp;**`Meiotextura e menu e logo`** Serve para caregar uma imagem para a tela 

 &nbsp;&nbsp;&nbsp;&nbsp;**`Texto`** Esta variavel permite escrever texto na tela

 &nbsp;&nbsp;&nbsp;&nbsp;**`ganhador`** È um vetor que permite pegar a posição (x,y)


### Métodos  

&nbsp;&nbsp;&nbsp;&nbsp;**`Initialize`**  Define a largura e altura da janela (Posicao) .

&nbsp;&nbsp;&nbsp;&nbsp;**`LoadContent`** Verifica os inputs do jogador, move a bola, verifica se a bola ultrapaçou os limites da tela , e atualiza a pontuação


&nbsp;&nbsp;&nbsp;&nbsp;**`Draw`** Limpa a tela, desenha o main menu, placar, jogadores, bola e a linha divisoria exibe tambem os fps e renicia o jogo caso um jogador chegue a pontuação maxima






<br>
</br>

***


