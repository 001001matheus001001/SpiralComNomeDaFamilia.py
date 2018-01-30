# SpiralComNomeDaFamilia.py
#Script em python3 feito por Matheus Silva
#30/01/2018 Hs 02:30 
#Dependencias Python3 + python-tk
#Valeu ae galera. 

# Importa os graficos tartaruga

import turtle
t = turtle.Pen()
turtle.bgcolor("black")
cores =["red", "yellow", "blue", "green", "orange", "purple", "white", "brown", "gray", "pink"]
familia = []

# Pede o primeiro nome ->
nome = turtle.textinput("My family",
                       "Entre com o nome da sua familia [ENTER] OU QUIT :")
# Continua pedindo nomes ->
while nome != "":
    #Adiciona o nome a lista de familiares
    familia.append(nome)
    nome = turtle.textinput("My family",
                            "entre com o nome da sua familia [ENTER] OU QUIT :")

# Desenha  uma espiral na tela, com os nomes

for x in range(100):
    t.pencolor(cores[x%len(familia)])
    t.penup()
    t.forward(x*4)
    t.pendown()
    t.write(familia[x%len(familia)], font = ("Arial", int((x+4)/4), "bold") )
    t.left(360/len(familia) +2)
