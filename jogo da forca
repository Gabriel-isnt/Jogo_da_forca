from random import choice

frutas = [
    'maça', 'banana', 'laranja', 'abacaxi', 'morango',
    'uva', 'pera', 'kiwi', 'melancia', 'melao',
    'limao', 'cereja', 'framboesa', 'manga', 'pessego',
    'goiaba', 'caju', 'abacate', 'figo', 'amora'
]


def verifica_entrada() -> str:
    while True:
        a = str(input(': ').strip().lower())

        if len(a) != 1 or a.isnumeric():
            print('\033[91mdigite apenas uma letra...\033[0m')
        else:
            return a


def jogar() -> None:
    while True:
        palavra = choice(frutas)
        tentativas = 7
        visual = ['_'] * len(palavra)
        print(f"\033[94m{' '.join(visual)}\033[0m")

        while tentativas > 0 and '_' in visual:
            print('digite uma letra qualquer')
            esc_letra = verifica_entrada()

            if esc_letra in palavra:
                for indice, letra in enumerate(palavra):
                    if letra == esc_letra:
                        visual[indice] = letra

                print(f"\033[94m{' '.join(visual)}\033[0m")

            else:
                print('\033[91mnão tem essa letra na palavra...\033[0m')
                print(f"\033[94m{' '.join(visual)}\033[0m")
                tentativas -= 1

        print(f'fim de jogo\nPalavra escolhida: {palavra}')

        continuar = str(input('deseja jogar de novo? [s / n] \n>>: ').strip().lower())
        if continuar in ['n', 'não', 'nao']:
            break


jogar()
