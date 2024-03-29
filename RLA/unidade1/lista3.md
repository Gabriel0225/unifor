
# UNIFOR
**Nome**: Nome do estudante <br>
**Disciplina**: Raciocínio lógico algorítm

## Exercício exemplo 1
Implemente e teste um programa que imprima os n primeiros números.

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[\n\]
C --> D[\num = 1\]
D --> E{num <= n}
E --FALSE--> I([FIM])
E --TRUE--> F{{"Num", num}}
F --> G[num =+ 1]
G --LOOP--> E
```

#### Pseudocódigo
```
1 ALGORITMO print_n_primeiros
2 DECLARE n, num: INTEIRO
3 INICIO
4 ESCREVA “Digite um número: ”
4 LEIA n			// variável de entrada n
4 num ← 1			// variável num inicializada
5 ENQUANTO num <= n FAÇA	// n iterações
7	ESCREVA “Número ”, num
8	num ← num + 1		// num =+ 1 (incremento)
8 FIM_ENQUANTO
9 FIM
```

#### Teste de mesa
| it | n  | num | num <= n | Saída      | num =+ 1 |
| -- | -- | --  | --       | --         | --       |
| 1  | 10 | 1   | True     | Número 1   | 2        |
| 2  | 10 | 2   | True     | Número 2   | 3        |
| 3  | 10 | 3   | True     | Número 3   | 4        |
| 4  | 10 | 4   | True     | Número 4   | 5        |
| 5  | 10 | 5   | True     | Número 5   | 6        |
| 6  | 10 | 6   | True     | Número 6   | 7        |
| 7  | 10 | 7   | True     | Número 7   | 8        |
| 8  | 10 | 8   | True     | Número 8   | 9        |
| 9  | 10 | 9   | True     | Número 9   | 10       |
| 10 | 10 | 11  | True     | Número 10  | 11       |
| 11 | 10 | 11  | False    |            |          |

## Exercício exemplo 2
Implemente e teste um programa que some os n primeiros números.

#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número: }}
B --> C[\n\]
C --> D[\soma = 0\]
D --> E[[i=1 ATÉ n PASSO 1]]
E --FALSE--> G([FIM])
E --TRUE--> F[soma =+ i]
F --LOOP--> E
```

#### Pseudocódigo
```
1  ALGORITMO	soma_n_numeros()
2  DECLARE	n, i, soma: INTEIRO
3  INICIO
4  ESCREVA “Digite a quantidade de números: ”
5  LEIA n		// variável de entrada n
7  soma ← 0		// variável soma inicializada
6  PARA i DE 1 ATÉ n PASSO 1 FAÇA
7	soma ← soma + i	// soma =+ i (incremento)
8  FIM_PARA
9  ESCREVA “A soma é igual a ”, soma
10 FIM
```

#### Teste de mesa
| it | n  | soma | i  | soma =+ i |
| -- | -- | --   | -- | --        |
| 1  | 10 | 0    | 1  | 1         |
| 2  | 10 | 1    | 2  | 3         |
| 3  | 10 | 3    | 3  | 6         |
| 4  | 10 | 6    | 4  | 10        |
| 5  | 10 | 10   | 5  | 15        |
| 6  | 10 | 15   | 6  | 21        |
| 7  | 10 | 21   | 7  | 28        |
| 8  | 10 | 28   | 8  | 36        |
| 9  | 10 | 36   | 9  | 45        |
| 10 | 10 | 45   | 10 | 55        | 

## Lista de exercícios 03

### Exercício 01 (2.5 pontos)
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero. 

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número positivo: }} --> C[/N/] --> D{N >= 0} --> I{{Este número não é positivo. Digite outro: }} --LOOP-->D
D --TRUE--> E{N % 2 == 0} --TRUE--> F{{Este número é par}} --> H([FIM]) 
E --FALSE--> G{{Este número é ímpar}} --> H
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ClassificaCategoria
var
   N, I: Inteiro
inicio
      Escreva ("Digite um número positivo: ")
      Leia (N)
      Se (N < 0) entao
         Repita
               Escreva ("Este número não é positivo. Digite outro: ")
               Leia (N)
         ate N >= 0
      FimSe
      Se (N % 2 = 0) entao
         Escreva ("Este número é par.")
      Senao
           Escreva ("Este número é ímpar.")
      FimSe
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| nome_coluna1 | nome_coluna2 | nome_coluna3 | nome_coluna4 | nome_coluna5 | 
|      --      |      --      |      --      |      --      |      --      | 
| Adicione     | espaço       | se quiser    |  alinhar     | as barras    |
| verticais,   | mas          | não é        | obrigatório. | Entendido ?  |

### Exercício 02 (2.5 pontos)
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) 
A --> D[\num = 0\]
D --> E{num <= 30}
E --FALSE--> I([FIM])
E --TRUE--> F{{"Num", 0}}
F --> G[num =+ 3]
G --LOOP--> E
```

#### Pseudocódigo (1.0 ponto)

```
algoritmo "print_n_primeiros"
 var
    n, num: INTEIRO
 inicio
       num <- 0
       ENQUANTO num <= 30 FAÇA
      	ESCREVAL("Número ", num)
      	num <- num + 3
       FIMENQUANTO
 Fimalgoritmo
```

#### Teste de mesa (0.5 ponto)

| nome_coluna1 | nome_coluna2 | nome_coluna3 | nome_coluna4 | nome_coluna5 | 
|      --      |      --      |      --      |      --      |      --      | 
| Adicione     | espaço       | se quiser    |  alinhar     | as barras    |
| verticais,   | mas          | não é        | obrigatório. | Entendido ?  |

### Exercício 03 (2.5 pontos)
Dada uma sequência de números inteiros, calcular a sua soma. 
Por exemplo, para a sequência {12, 17, 4, -6, 8, 0}, o seu programa deve escrever o número 35.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> K[S <- 0] --> L[cont <- 0] --> B{{"Quantos valores você quer somar? "}} --> C[/V/] --> D{cont <= V} --TRUE--> E{{"Digite um número"}} --> F[/N/]
F --> G[S <- S + N] --> H[cont <- cont + 1] --> D
D --FALSE--> I{{"A soma foi ", S}} --> J([FIM])
```

#### Pseudocódigo (1.0 ponto)

```
algoritmo "SOMA"
var
   S, N, V, cont: Inteiro
inicio
      Escreva ("Quantos valores você quer somar? ")
      Leia (V)
      S <- 0
      Enquanto cont <= V faca
          Escreva ("Digite um número: ")
          Leia (N)
          S <- S + N
          cont <- cont + 1
      FimEnquanto
      Escreval("A soma desses valores foi ", S)
fimalgoritmo
```

#### Teste de mesa (0.5 ponto)

| nome_coluna1 | nome_coluna2 | nome_coluna3 | nome_coluna4 | nome_coluna5 | 
|      --      |      --      |      --      |      --      |      --      | 
| Adicione     | espaço       | se quiser    |  alinhar     | as barras    |
| verticais,   | mas          | não é        | obrigatório. | Entendido ?  |

### Exercício 04 (2.5 pontos)
Escreva um programa que leia a nota de diversos alunos, até que seja digitada uma nota negativa. 
Nesse momento, ele mostra a média aritmética de todas as notas lidas e quantas notas foram lidas. 
Ex. Foram lidas 14 notas. A média aritmética é 6.75!

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([INICIO]) --> C[cont = 0]
C --> K{{"Digite uma nota"}}
K --> N[/nota1/]
N --> B[soma = nota1]
B --> D{nota1 >= 0}
D --TRUE--> E{{"Digite outra nota"}}
E --> F[/nota/]
F --> G[cont = cont + 1]
G --> P[soma_ant = soma - nota]
P --> H[media = soma_ant / cont]
H --> I{nota < 0}
I --FALSE/LOOP--> E
D --FALSE--> O([FIM])
I --> J{{"A média foi de ", media:3:2}}
J --> L{{"Foram lidas ", cont}}
L --> M{{" notas"}}
M --> O
```

#### Pseudocódigo (1.0 ponto)

```
algoritmo "media_notas"
var
   soma, media, nota, nota1: REAL
   cont: INTEIRO
inicio
      cont <- 0 
      ESCREVA ("Digite a nota de um aluno: ")
      LEIA (nota1)
      soma <- nota1
      SE (nota1 >= 0) ENTAO
            REPITA
               ESCREVA ("Digite a nota de outro aluno: ")
               LEIA (nota)
               soma <- soma + nota
               cont <- cont + 1
            ATE (nota < 0)
            media <- (soma - nota) / cont
         ESCREVAL("A média foi ", media:3:2)
         ESCREVAL("Foram lidas ", cont, " notas")
      FIMSE
fimalgoritmo
```

#### Teste de mesa (0.5 ponto)

| nota         | cont         | soma         | nota < 0     | media        |        
|      6.5     |      0       |      6.5     |     FALSE    |      --      | 
|      8.6     |      1       |     15.1     |     FALSE    |     2.10     |
|      7.4     |      2       |     22.5     |     FALSE    |     7.55     |
|      -1      |      3       |     21.5     |     TRUE     |     7.50     |
