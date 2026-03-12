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





9. Verificação de CPF: Leia um CPF no formato xxx.xxx.xxx-xx e valide os dígitos verificadores.



10. Número por extenso: Leia um número até 99 e mostre-o por extenso.



11. Jogo da Forca: Desenvolva um jogo simples da forca usando uma lista de palavras.

12. Corrigir telefone: Leia um telefone com 7 ou 8 dígitos e ajuste adicionando o '3' se necessário.

13. Palavra embaralhada: Mostre uma palavra com letras embaralhadas e permita que o usuário
adivinhe.

14. Leet Speak: Leia um texto e converta para a escrita estilo leet (ex: 1337).
