# Calculadora-Simples-
#Calculadora criada com conceitos iniciais de python 
from time import sleep

# Função de soma
def somar_numeros(a, b):
    soma = a + b
    return soma

# Função de subtração
def subtrair_numeros(a, b):
    subtrair = a - b
    return subtrair

# Função de multiplicação
def multiplicar_numeros(a, b):
    multiplicar = a * b
    return multiplicar

# Função de divisão
def dividir_numeros(a, b):
    dividir = a / b
    return dividir

resposta = "S"  

print("Olá, me chamo ENTITY, qual é o seu nome?")

nome = input("Digite seu nome para continuar: ")
print(f"Prazer {nome}, qual operação você quer realizar")
print("|+  pressione 1|\n|-  pressione 2|\n|x  pressione 3|\n|/  pressione 4|")


while resposta == "S":
    while True:
        operacao = input("Digite a operação: ")
        if operacao in ('1', '2', '3', '4', '5'):
            break
        else:
            print("Opção inválida. Escolha uma opção listada acima.")



    if operacao == '1':
        print("Você escolheu adição")
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        resultado = somar_numeros(num1, num2)
        print(f"O resultado da adição é: {resultado}")


    elif operacao == '2':
        print("Você escolheu subtração")
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        resultado = subtrair_numeros(num1, num2)
        print(f"O resultado da subtração é: {resultado}")


    elif operacao == '3':
        print("Você escolheu multiplicação")
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        resultado = multiplicar_numeros(num1, num2)
        print(f"O resultado da multiplicação é: {resultado}")


    elif operacao == '4':
        print("Você escolheu divisão")
        num1 = float(input("Digite o primeiro número: "))
        num2 = float(input("Digite o segundo número: "))
        while num2 == 0:
            num2 = float(input("Ops, algo deu errado. Digite um valor válido para o segundo número: "))
        print(f"Resultado = {num1 // num2}")



    resposta = input(f"{nome}, deseja fazer mais alguma operação? [S / N ]: ").upper()

print("Programa encerrado. Obrigado por utilizar meus sistemas! (>_<)")
            
