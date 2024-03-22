# UNIFOR
**Nome**: Gabriel Musashi Miyazawa
**Disciplina**: Raciocínio lógico algorítmico

## Lista de exercícios 01

### Exercício 3
Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um número inteiro e positivo é par ou impar.

#### Fluxograma

``` mermaid
flowchart TD
A([START]) --> B{{Write a number}} 
B --> C[/num/]
C --> D{num >= 0}
D --NOT--> E{{The number must be positive}}
D --YES--> G{num % 2 == 0}
G --YES--> H{{PAIR}}
G --NOT--> I{{ODD}}
H --> F
I --> F
E --> F([END])
```
#### Pseudocódigo
```
ALGORITMO verifica_par_impar
DECLARE num: INTEIRO
INICIO
	ESCREVA "Digite um número: "
	LEIA num
	SE num >= 0 ENTAO
		SE num % 2 == 0 ENTAO
			ESCREVA "O número é par"
		SENAO
			ESCREVA "O número é ímpar"
		FIMSE
	SENAO
		ESCREVA "O número deve ser positivo"
	FIMSE
FIMALGORITMO
```

 #### Teste
 | num | num >= 0 | resto | resto == 0 | Saída |
 | -- | -- | -- | -- | -- | 
 | -1 | False |  |  |"O número deve ser positivo"
 | 0 | True | 0 | True |"O número é par"
 | 10 | True | 0 | True |"O número é par"
 | 11 | True | 1 | False |"O número é ímpar" 
