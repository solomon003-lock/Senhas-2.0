
import pandas as pd
import string

senha_input= input("Digite uma senha:")
tamanho =  len(senha_input)
senha = list(senha_input)
print(tamanho)
print(senha)

alfabeto = [ "a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","x","z","w","y"]
i=0
adivinha = []

for i in range(0,(tamanho)):
    adivinha.append(("a"))
print("adivinha agora é :" , adivinha)

i=0
a=0
k = tamanho-1
while adivinha[k] != senha[k]:
  if (senha[a] != alfabeto[i]) is True:
    print("i é igual a  ", i, "a é igual a ", a , "diferente") #linha para imprimir na tela as interações e tentar identificar o erro
    i = i+1
  else:
    adivinha[a]=alfabeto[i]
    print( "a é igual a ", a ,"i é igual a  ", i,"igual", adivinha) #linha para imprimir na tela as interações e tentar identificar o erro

    i = 0
    a=a+1

print("A senha digitada é: ",adivinha)
