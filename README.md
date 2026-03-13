# Lista-de-Exercicios-Strings-Python-
1. Tamanho de strings: Leia duas strings, mostre o conteúdo e o tamanho de cada uma. Informe se
possuem o mesmo tamanho e se o conteúdo é igual ou diferente.

letra1 = (input())
letra2 = (input())

igual = letra1 == letra2
tam = len(letra1)
tam2 = len(letra2)
print(f'palavra:{letra1}, tamanho: {tam}')
print(f'palavra:{letra2}, tamanho: {tam2}')
print(f'são iguais: {igual}')

2. Nome ao contrário em maiúsculas: Leia o nome do usuário e mostre-o de trás para frente em
letras maiúsculas.
letra1 = (input())

letra1 = letra1.upper()
letra1 = letra1[::-1]

print(f'são iguais:{letra1}')


3. Nome na vertical: Solicite o nome do usuário e imprima cada letra em uma linha.
  letra1 = (input())

for letra in letra1:
    print(letra)




4. Nome em escada: Mostre o nome em formato de escada crescente (F, FU, FUL...).
letra1 = (input())

for p in range(1, len(letra1) +1 ):
  print(letra1[:p])

5. Escada invertida: Mostre o nome em escada decrescente.

letra1 = (input())
n = len(letra1)

for p in range(1, len(letra1) +1 ):

   print(letra1[:-p])

6. Data por extenso: Leia uma data (dd/mm/aaaa) e mostre no formato '29 de Outubro de 1973'.

print('Informe uma data.')
dia = (input('Informe um dia DD: '))
mes = (input('Informe um mes MM: '))
ano = (input('Informe um ano MM: '))

if mes == "01":
    print(f'{dia} de Janeiro de {ano}')
elif mes == "02":
    print(f'{dia} de Fevereiro de {ano}')
elif mes == "03":
    print(f'{dia} de Março de {ano}')
elif mes == "04":
    print(f'{dia} de Abril de {ano}')
elif mes == "05":
    print(f'{dia} de Maio de {ano}')
elif mes == "06":
    print(f'{dia} de Junho de {ano}')
elif mes == "07":
    print(f'{dia} de Julho de {ano}')
elif mes == "08":
    print(f'{dia} de Agosto de {ano}')
elif mes == "09":
    print(f'{dia} de Setembro de {ano}')
elif mes == "10":
    print(f'{dia} de Outubro de {ano}')
elif mes == "11":
    print(f'{dia} de Novembro de {ano}')
elif mes == "12":
    print(f'{dia} de Dezembro de {ano}')

7. Contar espaços e vogais: Dada uma frase, conte quantos espaços existem e quantas vezes
aparecem as vogais.
letra = "Professor odair é o melhor professor da faculdade "
o = 0
e = letra.count(' ')
for i in letra:
    #i = i.lower()
    if i == 'a' or i == "e" or i =='i' or i =='o' or i=='u': 
        o += 1
      
print(f'Voce teve {o} Vogais')
print(f'voce teve {e} espaçõs' )



8. Palíndromo: Leia uma sequência de caracteres e informe se é um palíndromo.

frase = input("Digite uma palavra ou frase: ")

frase_limpa = frase.replace(" ", "").lower()
frase_invertida = frase_limpa[::-1]

if frase_limpa == frase_invertida:
    print(f"'{frase}' é um palíndromo!")
else:
    print(f"'{frase}' não é um palíndromo.")




9. Verificação de CPF: Leia um CPF no formato xxx.xxx.xxx-xx e valide os dígitos verificadores.
cpf = input("Digite apenas os números do CPF: ")

c = 10
total = 0
for i in cpf[:9]:
    total += int(i) * c
    c -= 1

digito1 = (total * 10) % 11
if digito1 == 10:
    digito1 = 0

c = 11
total = 0
for i in cpf[:10]:
    total += int(i) * c
    c -= 1

digito2 = (total * 10) % 11
if digito2 == 10:
    digito2 = 0

calculados = f"{digito1}{digito2}"

if calculados == cpf[9:]:
    print(f"O CPF {cpf} é VÁLIDO! ")
else:
    print(f"O CPF {cpf} é INVÁLIDO! ")


10. Número por extenso: Leia um número até 99 e mostre-o por extenso.


unidades = ["zero", "um", "dois", "três", "quatro", "cinco", "seis", "sete", "oito", "nove"]
dezenas = ["", "", "vinte", "trinta", "quarenta", "cinquenta", "sessenta", "setenta", "oitenta", "noventa"]
especiais = ["dez", "onze", "doze", "treze", "quatorze", "quinze", "dezesseis", "dezessete", "dezoito", "dezenove"]

num = int(input("Digite um número entre 0 e 99: "))

if 0 <= num <= 9:
    print(unidades[num])

elif 10 <= num <= 19:
    print(especiais[num - 10])

elif 20 <= num <= 99:
    d = num // 10  
    u = num % 10   
    
    if u == 0:
        print(dezenas[d])
    else:
        print(f"{dezenas[d]} e {unidades[u]}")
else:
    print("Número fora do intervalo!")


11. Jogo da Forca: Desenvolva um jogo simples da forca usando uma lista de palavras.

palavra_secreta = "python"
letras_acertadas = ["_"] * len(palavra_secreta)
tentativas = 6
letras_digitadas = []

while tentativas > 0 and "_" in letras_acertadas:
    print(f"\nPalavra: {' '.join(letras_acertadas)}")
    print(f"Tentativas restantes: {tentativas}")
    
    chute = input("Digite uma letra: ").lower()

    if chute in letras_digitadas:
        print("Você já tentou essa!")
        continue

    letras_digitadas.append(chute)

    if chute in palavra_secreta:
        indice = 0
        for letra in palavra_secreta:
            if chute == letra:
                letras_acertadas[indice] = chute
            indice += 1
    else:
        tentativas -= 1
        print("Errou!")

if "_" not in letras_acertadas:
    print(f"\nGanhou! A palavra era: {palavra_secreta}")
else:
    print(f"\nPerdeu! A palavra era: {palavra_secreta}")

12. Corrigir telefone: Leia um telefone com 7 ou 8 dígitos e ajuste adicionando o '3' se necessário.

telefone = input("Digite o telefone: ")

if len(telefone) == 7:
    novo_telefone = "3" + telefone
    print(f"Telefone corrigido: {novo_telefone}")
elif len(telefone) == 8:
    print(f"Telefone correto: {telefone}")
else:
    print("Número inválido! Digite 7 ou 8 dígitos.")

13. Palavra embaralhada: Mostre uma palavra com letras embaralhadas e permita que o usuário
adivinhe.

palavra_correta = "python"
palavra_embaralhada = "typhon" 

print(f"A palavra embaralhada é: {palavra_embaralhada}")

tentativa = input("Qual é a palavra correta? ").lower()

if tentativa == palavra_correta:
    print("Parabéns! Você acertou.")
else:
    print(f"Errado! A palavra era {palavra_correta}.")

14. Leet Speak: Leia um texto e converta para a escrita estilo leet (ex: 1337).

texto = input("Digite um texto para converter: ").upper()

texto = texto.replace("A", "4")
texto = texto.replace("E", "3")
texto = texto.replace("I", "1")
texto = texto.replace("O", "0")
texto = texto.replace("T", "7")
texto = texto.replace("S", "5")

print(f"Texto em Leet Speak: {texto}")
