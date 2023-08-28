from time import sleep

# Texto inicial
print('\n\033[34m----Bem Vindo a Calculadora de Texto----\033[m')
print('\033[31;4;1mDescrição:\033[m \033[37mAqui você pode colocar um texto e ver a \033[36;4mporcentagem\033[m \n\033[37mdos seus \033[32;4macertos!\033[m\n')

# Calculando a quantidade de palavras
texto = str(input('\033[33m*Insira seu texto: \033[m')).strip()
erradas = int(input('\033[33m*Insira a quantidade de \033[31;1;4mpalavras erradas:\033[m '))
resultado = len(texto.split())

# Adicionando um delay
print('\033[35mCarregando as Informações...\033[m\n')
sleep(2)

# Calculando a porcentagem
porcentagem = (resultado - erradas) * 100 / resultado

# Saída
print('\033[37m*Existem \033[36;1;4m{} palavras\033[m \033[37mnesse texto e \033[31;1;4m{} delas estão erradas ou incompletas!\033[m'.format(resultado, erradas))
sleep(0.70)
print('\033[32;1m*Porcentagem de acertos: {:.1f}%\033[m'.format(porcentagem))
sleep(0.70)

# Saídas personalizadas
if porcentagem < 50:
    print('\033[33m--- Você precisa se esforçar mais :( ---\033[m')

if porcentagem >= 50:
    if porcentagem < 80:
        print('\033[36m--- Parabéns! Continue assim :) ---\033[m')

if porcentagem > 80: print('\033[32m--- Wooow look at him! Advance more, kid ;) ---\033[m')
