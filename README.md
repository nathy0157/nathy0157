#trabalho pac man
import turtle 
import Keyboard

tela = turtle.Screen()  # Criação da tela
tela.bgcolor("orangeyellow")  # Cor da tela laranja amarelado

# Criação dos jogadores 1 e 2
player1 = turtle.Turtle()
player2 = turtle.Turtle()

# Configuração do player1 
player1.shape("turtle")  # Formato da tartaruga
player1.color("black")  # Cor da tartaruga
player1.penup()  # penup é uma variável onde faz com que as tartarugas não deixem rastros de linha na tela
player1.speed(4)
player1.setposition(-100, 0)  # Posição inicial do jogador 1

# Configuração player2
# Configurações para o jogador 2
player2.shape("turtle")  # Formato da tartaruga
player2.color("white")  # Cor do corpo da tartaruga
player2.penup() 
player2.speed(4)
player2.setposition(100, 0)  # Posição inicial do jogador 2

# Funções para mover a tartaruga dos players usando as teclas (w, s, a, d)
# Função do primeiro jogador
def moverp_cimapl1():
    player1.setheading(90)  # Direção para cima, o "90", é o ângulo determinado que a tartaruga vai seguir
    player1.forward(5)  # Esse 5 é o tanto de passos que a tartaruga irá dar
    
def moverp_esquerdapl1():
    player1.setheading(180)  # Direção para a esquerda, o "180", é o ângulo determinado que a tartaruga vai seguir
    player1.forward(5)
    
def moverp_direitapl1():
    player1.setheading(0)  # Direção para a direita, o "0", é o ângulo determinado que a tartaruga vai seguir
    player1.forward(5)
    
def moverp_baixopl1():
    player1.setheading(270)  # Direção para baixo, o "270", é o ângulo determinado que a tartaruga vai seguir
    player1.forward(5)

# Funções para mover a tartaruga dos players usando as teclas (CIMA, BAIXO, ESQUERDA, BAIXO)
# Função do segundo jogador
def mover_cimapl2():
    player2.setheading(90)  # Direção para cima
    player2.forward(5)
    
def moverp_esquerdapl2():
    player2.setheading(180)  # Direção para a esquerda
    player2.forward(5)
    
def moverp_direitapl2():
    player2.setheading(0)  # Direção para a direita
    player2.forward(5)
    
def moverp_baixopl2():
    player2.setheading(270)  # Direção para baixo
    player2.forward(5)

# Leitura das teclas do (W, S, A, D)
tela.listen()  # Inicia a escuta do teclado
# A função onkey faz com que leia as teclas de movimento
Keyboard.onkey(moverp_cimapl1, "w")  # Quando pressionar W, move para cima
Keyboard.onkey(moverp_baixopl1, "s")  # Quando pressionar S, move para baixo
Keyboard.onkey(moverp_esquerdapl1, "a")  # Quando pressionar A, move para a esquerda
Keyboard.onkey(moverp_direitapl1, "d")  # Quando pressionar D, move para a direita

# Leitura das teclas do (SETAS UP, RIGHT, LEFT, DOWN)
tela.listen()
Keyboard.onkey(mover_cimapl2, "Up")  # Quando pressionar seta para cima, move para cima
Keyboard.onkey(moverp_baixopl2, "Down")  # Quando pressionar seta para baixo, move para baixo
Keyboard.onkey(moverp_direitapl2, "Right")  # Quando pressionar seta para a direita, move para a direita
Keyboard.onkey(moverp_esquerdapl2, "Left")  # Quando pressionar seta para a esquerda, move para a esquerda
