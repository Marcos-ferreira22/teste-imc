import time

usario = ''
inicio = True
teste = ''

while inicio:
    usuario = str(input('digite seu nome: '))
    if usuario.isalpha():
        time.sleep(0.7)
        print(f'praser em te conhecer: {usuario} ')
    else:
        print(f'por favor digite seu nome corretamente {usuario} não e um nome')
    break

time.sleep(0.5)
print(f'{usuario} voce deseja faser alguns testes comigo?:')

while teste != "S" or "N":
    teste = str(input(f'''digite  apenas  
    [s] para sim  e 
    [n] para não 
    resposta:  ''')).capitalize()
    print('verificando resposta....')
    time.sleep(0.7)
    if teste == 'N':
        print('voce escolheu nao continuar')
        print(f'muito obrigado pela atenção {usuario} ate mais')
        break

    elif teste == 'S':
        time.sleep(0.7)
        print('certo')
        time.sleep(0.7)
        print('vamos começar? ')
        peso = float(input('qual é o seu peso? '))
        altura = float(input('qual e a sua alura? '))
        idade = int(input('qual é a sua idade? '))
        imc = peso / (altura * 2)
        ml = 0.035
        quan_agua = peso * ml
        if imc < 16:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
             voce esta com magreza grave voce deve se cuidar mais''')
        elif imc >= 16 and imc <=17:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
            voce esta com magresa morbida voce deve se
            cuidar mais''')
        elif imc >17 and imc <=18.5:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
            voce esta mcom magreza leve voce deve se cuidar mais''')
        elif imc >18.5 and imc <=25:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
            voce estanormal parabens''')
        elif imc >25 and imc <=30:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
            voce esta com sobre peso voce deve se cuidar mais''')
        elif imc > 30 and imc <=35:
            time.sleep(0.7)
            print(f'''seu indice de maca corporal e de {imc :.2f}
             voce esta com obesidade grau 1 voce deve se cuidar mais''')
        elif imc > 35 and imc <=40:
            time.sleep(0.7)
            print(f'''seu indeice de maca corporal e de {imc :.2f}
             voce esta com obesidade grau 2 (severa) voce deve se cuidar mais''')
        else :
            time.sleep(0.7)
            print(f'''seu indeice de maca corporal e de {imc :.2f}
             voce esta com obesidade grau 3 (morbida) voce deve se cuidar mais''')
        time.sleep(0.7)
        print('e tambem')
        time.sleep(0.7)
        print(f'voce deve beber cerca de {quan_agua:.2f}litros de agua por dia')
        break


