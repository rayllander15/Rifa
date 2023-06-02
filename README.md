import random
from time import sleep
lista = {}
sorteio = list()
print('\033[33m-=\033[m'*20)
print(f'\033[36m{"Sorteio da DOCE MEL":^35}\033[m')
print('\033[33m-=\033[m'*20)
while True:
    lista["nome"]= str(input('\033[3:34mNome do participante: \033[m'))
    lista["número"]=int(input(f'\033[3:34mNúmero que\033[m \033[33m{lista["nome"]}\033[m \033[3:34mescolheu para ser sorteado: \033[m'))
    sorteio.append(lista.copy())
    while True:
        r = str(input('\033[35mContinuar?[S/N]: \033[m')).upper().strip()[0]
        if r in 'SN':
          break
        print('\033[31mVcoê digitou errado, por favor digite apenas S ou N!\033[m')
    if r == 'N':
         break
print(f'\033[33m{"Participantes ":<4} {"Número da rifa":>20}\033[m')
for c,d in enumerate(sorteio):
    print(f'{c+1}ª {d["nome"]:<4}, {d["número"]:>20}')
    sleep(0.8)
print('\033[33m=\033[m'*30)
print(f'\033[36m{"BOA SORTE NO SORTEIO!":^30}\033[m')
print('\033[33m=\033[m'*30)
print(random.choice(sorteio))
sleep(1)

