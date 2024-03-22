
Skip to content

    Pricing

Sign in
Sign up
Px1906 /
unifor
Public

Code
Issues
Pull requests
Actions
Projects
Security

    Insights

Commit
Update AD1.md

    main 

@Px1906
Px1906 committed Mar 20, 2024
1 parent 137fbe9 commit 890ef84
Showing 1 changed file with 2 additions and 2 deletions.

4 changes: 2 additions & 2 deletions 4
RLA/AD1.md

Curso: Engenharia da Computação
Disciplina: Raciocinio Lógico e ALgorítimo
Código/Turma: T998-21
Professor: Ricardo Carubbi
Data: 20/03
Aluno(a): Sergio de Paiva Ximenes Filho
Matrícula: 2410330

1a chamada (Sim/Não): preencha com a opção correta
2a chamada (Sim/Não): preencha com a opção correta

1a chamada (Sim/Não): sim
2a chamada (Sim/Não): não
Avaliação Diagnóstica 1
Normas e exigências

Avaliação diagnóstica (AD) consiste em exercícios ou projetos desenvolvidos em grupo ao longo da disciplina.
A primeira avaliação diagnóstica (AD1) será composta por exercícios e equivale a 30% da nota da primeira avaliação (AV1).

Segue abaixo a expressão para o cálculo da AV1, sendo sendo AF1 equivale a primeira avaliação formativa e AD1, a primeira avaliação diagnóstica.

A AD1 é formada pela entrega dos exercícios (EX1) na data prevista e apresentação (AP1) de um dos exercícios escolhido pelo professor. Segue abaixo a expressão para o cálculo da AD1.

A EX1 é avaliada mediante a correção dos exercícios, sendo a avaliação no intervalo de 0% (não atende a questão), 50% (atende parcialmente) e 100% (atende em sua totalidade). Por exemplo, se o exercício equivale a 2 pontos e sua correção atente parcialmente a questão, então sua avaliação deste exercício será 1 ponto.

A AP1 é avaliada mediante aos pré-requisitos de clareza, organização e domínio do conteúdo. Portanto, o aluno deve demonstrar um bom entendimento do algoritmo, explicando seus princípios fundamentais, seu propósito e como ele funciona passo a passo.

A avaliação da AP1 é apenas considerada no intervalo de 0% (não atende os pré-requisitos), 25% (pouco atende os pré-requisitos), 50% (atende de forma mediana os pré-requisitos), 75% (atende de forma razoável os pré-requisitos) e 100% (atende em a totalidade dos pré-requisitos). Por exemplo, se na apresentação do exercício, o aluno atenter de forma razoável a questão, então sua avaliação da apresentação será 7.5 pontos.
Datas

    Entrega da primeira avaliação formativa (AF1) composta pelas listas de exerciícios 1, 2 e 3: 21/03/24
    Entrega dos exercícios da primeira avaliação diagnóstica (EX1): 21/03/24
    Apresentação da primeira avaliação diagnóstica (AP1): 21/03/24

Lista de questões
Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis,
e

, implemente e teste um algoritmo para trocar os valores atribuídos a elas.
Descrição geral do algoritmo

    Guardar o valor original da variável 

em uma variável auxiliar
;
Atribuir à variável
o valor original da variável
;
Atribuir à variável
o valor original da variável , que está armazenado na variável auxiliar
.
Exibir os novos valores de
e

    .

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo TrocaValores
DECLARE A, B, Mem: float
INICIO
ESCREVA "Digite o valor de A"
LEIA A
ESCREVA "Digite o valor de B"
LEIA B
Mem = B
B = A
A = Mem
ESCREVA A, B
FIM_ALGORITMO

Teste de mesa
A 	B 	Mem = B 	B = A 	A = Mem 	Saida
10 	4 	4 	10 	4 	4, 10
Questão 2 - Contagem (1 ponto)

Dado um conjunto
de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem do número de alunos que foram aprovados no exame. Será considerado aprovado o aluno que tirar

50 ou maior (no intervalo de 0 a 100).
Descrição geral do algoritmo

    Obter o número de notas 

a serem processadas;
Inicializar a contagem
com zero;
Enquanto houver notas a serem processadas, fazer repetidamente:

    obter a próxima nota;
    se a nota for suficiente para passar no exame (

) então adicionar 1 (um) à contagem

    ;

Exibir a contagem

    (número total de aprovações).

Fluxograma 01

Fluxograma conforme descrição do algoritmo acima, usando o loop ENQUANTO.
Pseudocódigo 01 (1 ponto)

Algoritimo aprovação
DECLARE N_ver, N_aprov, N_notas, i: Int
	notas: Float
INICIO
N_aprov = 0 
ESCREVA "Digite a quanidade de notas para avaliar"
LEIA N_notas
ENQUANTO N_notas <= 0 REPITA
	ESCREVA "Digite uma quantidade válida"
	LEIA N_notas
PARA N_ver DE 1 ATÉ N_notas FAÇA [PASSO 1]
	ESCREVA "Insira a nota"
	LEIA nota
	SE nota >= 50 E nota <= 100
		N_aprov =+ 1
		N_ver =+ 1
	SENÃO
		N_ver =+ 1
	FIM_SE
FIM_PARA
ESCREVA "A quantidade de notas aprovadas foi", N_aprov
FIM_ALGORÍRIMO

Teste de mesa 01
Chat GPT
Iteração 	Ação 	Entrada/Saída 	N_aprov 	N_ver
	Inicialização das Variáveis 		0 	0
	Entrada do Número de Notas 	5 		
1 	Mensagem: "Insira a nota" 			
	Entrada: nota 	70 		
	Condição SE: 70 >= 50 e 70 <= 100 (verdadeiro) 			
	N_aprov += 1 		1 	1
	N_ver += 1 			1
2 	Mensagem: "Insira a nota" 			
	Entrada: nota 	30 		
	Condição SE: 30 >= 50 e 30 <= 100 (falso) 			
	N_ver += 1 			2
3 	Mensagem: "Insira a nota" 			
	Entrada: nota 	85 		
	Condição SE: 85 >= 50 e 85 <= 100 (verdadeiro) 			
	N_aprov += 1 		2 	3
	N_ver += 1 			3
4 	Mensagem: "Insira a nota" 			
	Entrada: nota 	95 		
	Condição SE: 95 >= 50 e 95 <= 100 (verdadeiro) 			
	N_aprov += 1 		3 	4
	N_ver += 1 			4
5 	Mensagem: "Insira a nota" 			
	Entrada: nota 	40 		
	Condição SE: 40 >= 50 e 40 <= 100 (falso) 			
	N_ver += 1 			5
- 	Saída de Resultados 			
- 	Mensagem: "A quantidade de notas aprovadas foi 3" 			
Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de
números, implemente e teste um algoritmo para calcular a soma desses números.
Aceite apenas

maior ou igual a zero.
Descrição geral do algoritmo

    Obter a quantidade de números 

a serem somados.
Inicializar a variável
com 0 (zero).
Enquanto menos do que
números tiverem sido somados, fazer repetidamente:

    obter o próximo número 

;
calcular a soma atual, adicionando o número

    obtido à soma mais recente;

Exibir a soma dos

    números

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo soma_de_valores
DECLARE num_somados, num_soma: Int
	num, soma: Float
INICIO
soma = 0
ESCREVA "Digite o número de elementos do conjunto que você quer somar"
LEIA num_soma
ENQUANTO num_soma <= 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA num_soma
FIM_ENQUANTO
PARA num_somados DE 1 até Num_soma [PASSO 1] FAÇA
	ESCREVA "Digite um número"
	LEIA num
	soma =+ num
FIM_PARA
ESCREVA "O valor da soma total é", soma
FIM_ALGORITMO

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	soma 	num_somados
- 	Inicialização das Variáveis 		0 	0
- 	Entrada do Número de Elementos a Somar 	7 		
1 	Mensagem: "Digite um número" 			
	Entrada: num 	0.5 		
	soma += num 		0.5 	
	num_somados += 1 			1
2 	Mensagem: "Digite um número" 			
	Entrada: num 	-1.25 		
	soma += num 		-0.75 	
	num_somados += 1 			2
3 	Mensagem: "Digite um número" 			
	Entrada: num 	2.75 		
	soma += num 		2 	
	num_somados += 1 			3
4 	Mensagem: "Digite um número" 			
	Entrada: num 	0 		
	soma += num 		2 	
	num_somados += 1 			4
5 	Mensagem: "Digite um número" 			
	Entrada: num 	-3.5 		
	soma += num 		-1.5 	
	num_somados += 1 			5
6 	Mensagem: "Digite um número" 			
	Entrada: num 	1.75 		
	soma += num 		0.25 	
	num_somados += 1 			6
7 	Mensagem: "Digite um número" 			
	Entrada: num 	-2.25 		
	soma += num 		-2 	
	num_somados += 1 			7
- 	Saída de Resultados 			
- 	Mensagem: "O valor da soma total é -2" 			
Questão 4 - Cálculo de uma série (1 ponto)

Dado um conjunto de

termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

Descrição geral do algoritmo

    Obter o número de termos 

;
Inicializar a variável
com 0 (zero).
Iterar o valor de
na variável iniciando com 0 (zero), de acordo com as instruções abaixo:

    calcular o numerador na variável 

;
calcular o denominador na variável
;;
calcular o termo da série na variável
, onde
;
adicionar esse termo à variável

    .

Exibir o valor da série

    .

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo soma_da_serie
DECLARE Num_termo, termo: Int
	S: Float
INICIO
S = 0
ESCREVA "Digite a quantidade de termos da série que você quer somar"
LEIA Num_termo // 3 
ENQUANTO Num_termo < 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA Num_termo
FIM_ENQUANTO
PARA termo DE 1 ATÉ Num_termo [PASSO 1] FAÇA
	S =+ (2 * termo - 1)/(2 * termo)
FIM_PARA
ESCREVA "O valor da soma de", Num_termo, "termo(s) da série é", S
FIM_ALGORITMO

Teste de mesa (0.25 ponto)
Chat GPT
Iteração 	Ação 	Entrada/Saída 	S
- 	Inicialização das Variáveis 		0
- 	Entrada do Número de Termos da Série 		
1 	Mensagem: "Digite a quantidade de termos da série" 		
	Entrada: Num_termo 		-3
			
2 	Verificação do Número de Termos 		
	Enquanto Num_termo < 0 FAÇA 		
	Mensagem: "Digite uma quantidade válida" 		
	Entrada: Num_termo 		
	FIM_ENQUANTO 		
			
- 	Saída de Resultados (Nenhum Cálculo Realizado) 		
- 	Mensagem: "O valor da soma de -3 termo(s) da série é" 		
	0 		
Questão 5 - Cálculo fatorial (2 pontos)

Dado um número
, implemente e teste um algoritmo para calcular o fatorial de (escrito como ), onde

.
Descrição geral do algoritmo

    Obter o número 

, onde
;
Inicializar a variável
com 1 (um) para armazenar o resultado do cálculo do fatorial;
Iterar o valor de
na variável , ou seja, executar vezes, as instruções abaixo:

    Incrementar o valor atual 

multiplicando pelo valor de

    ;

Exibir o resultado (

    ).

Fluxograma
Pseudocódigo (2 pontos)

Algoritmo fatorial
DECLARE fato, n_mult, n: Int
INICIO
n_mult = 0
ESCREVA "Digite o numero do fatorial que voce quer calcular"
LEIA n
ENQUANTO n < 0 FAÇA
	ESCREVA "Digite um fatorial válido"
	LEIA n
FIM_ENQUANTO
PARA n_mult DE 1 PARA n [PASSO 1] FAÇA
	n_mult =+ 1
	fato = fato * n_mult
FIM_PARA
ESCREVA "O valor do fatorial de", n, "é", fato 
FIM_ALGORITMO

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		0 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		-50 	
				
2 	Verificação da Validade do Número 			
	Mensagem: "Digite um fatorial válido" 			
	Entrada: n 		-50 	
				
- 	Saída do Resultado 			
- 	(nenhuma saída, pois o número não é válido) 			
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		1 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		1 	
				
2 	Verificação da Validade do Número 			
	(nenhuma ação necessária, 0 é válido) 			
				
- 	Saída do Resultado 			
- 	Mensagem: "O valor do fatorial de 0 é 1" 		1 	
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		1 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		6 	
				
2 	Verificação da Validade do Número 			
	(nenhuma ação necessária, 6 é válido) 			
				
3 	Cálculo do Fatorial 			
	n_mult = 1 			1
	fato = fato * n_mult 		1 	1
				
4 	n_mult = 2 			2
	fato = fato * n_mult 		1 	2
				
5 	n_mult = 3 			3
	fato = fato * n_mult 		2 	3
				
6 	n_mult = 4 			4
	fato = fato * n_mult 		6 	4
				
7 	n_mult = 5 			5
	fato = fato * n_mult 		24 	5
				
8 	n_mult = 6 			6
	fato = fato * n_mult 		120 	6
				
- 	Saída do Resultado 			
- 	Mensagem: "O valor do fatorial de 6 é 720" 		720 	
Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os
primeiros termos da sequência de Fibonacci, onde .
Os primeiros termos são:

. Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.
Descrição geral do algoritmo

    Obter o número de termos 

, onde
;
Inicializar os dois primeiros termos da série nas variável
e
com 0 (zero);
Iterar o valor de
, ou seja, executar vezes, as instruções abaixo:

    Imprimir o termo inicial 

(instrução para exibir a sequência ao atualizar a variável
);
Somar os termos
e na variável
;
Atribuir a variável
o valor da variável
;
Atribuir a variável
o valor da variável

        .

Fluxograma
Pseudocódigo (2 pontos)

Algoritimo fibonacci
DECLARE T1, T2, Tmem, TS, i: Int
INICIO
T1 = 0
T2 = 1
ESCREVA "Digite qual termo de fibonacci você quer calcular"
LEIA TS
ENQUANTO TS <= 0 FAÇA
	ESCREVA "Digite um termo válido"
	LEIA TS
FIM_ENQUANTO
PARA i DE 1 ATÉ TS [PASSO 1] FAÇA
	ESRCREVA T1
	Tmem = T1 + T2
	T1 = T2
	T2 = Tmem
FIM_PARA
FIM_ALGORITIMO

Teste de mesa
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					5
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					5
						
2 	Verificação da Validade do Número 					
	(nenhuma ação necessária, 5 é válido) 					
						
3 	Cálculo do Termo de Fibonacci 					
	PARA i DE 1 ATÉ 5 [PASSO 1] FAÇA 					
						
4 	i = 1 					
	Escreva: T1 		0 	1 		
						
	Tmem = T1 + T2 				1 	
	T1 = T2 		1 			
	T2 = Tmem 			1 		
						
5 	i = 2 					
	Escreva: T1 		1 	1 		
						
	Tmem = T1 + T2 				2 	
	T1 = T2 		1 			
	T2 = Tmem 			2 		
						
6 	i = 3 					
	Escreva: T1 		1 	2 		
						
	Tmem = T1 + T2 				3 	
	T1 = T2 		2 			
	T2 = Tmem 			3 		
						
7 	i = 4 					
	Escreva: T1 		2 	3 		
						
	Tmem = T1 + T2 				5 	
	T1 = T2 		3 			
	T2 = Tmem 			5 		
						
8 	i = 5 					
	Escreva: T1 		3 	5 		
						
	Tmem = T1 + T2 				8 	
	T1 = T2 		5 			
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					0
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					0
						
2 	Verificação da Validade do Número 					
	Mensagem: "Digite um termo válido" 					
	(Loop de entrada será repetido até que um número válido seja dado) 					
						
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					-90
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					-90
						
2 	Verificação da Validade do Número 					
	Mensagem: "Digite um termo válido" 					
	(Loop de entrada será repetido até que um número válido seja dado) 					
						
Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Implemente e teste um algoritmo para inverter a ordem dos dígitos de um número inteiro positivo.
Descrição geral do algoritmo

    Obter o número inteiro positivo 

a ser invertido;
Inicializar a variável
com 0 (zero);
Enquanto o número for maior que zero (
), faça repetidamente:

    Calcular o último dígito do número na variável 

;
Adicionar o dígito ao número invertido
;
Remover o último dígito do número original

        ;
    Exibir o número invertido.

Fluxograma
Pseudocódigo (2 pontos)

Algoritimo Inver
DECLARE Num, Num_inv, mem, mem2: Int
INICIO
ESCREVA "Digite o número que voce quer inverter"
LEIA Num
mem2 = Num
ENQUANTO Num <= 9 FAÇA
	ESCREVA "O número precisa ser positivo e ter mais de dois algarismos"
	ESCREVA "Digite o número que voce quer inverter"
FIM_ENQUANTO
ENQUANTO Num > 0 FAÇA
	mem = Num % 10
        Num =// 10
	Num_inv =* 10
	Num_inv =+ mem
FIM_ENQUANTO
ESCREVA "O número", mem2, "após inverter os algarismos é", Num_inv
FIM_ALGORITIMO 

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	Num 	Num_inv 	mem
- 	Inicialização 		12345 	0 	-
1 	Leitura do número a ser invertido 		12345 	0 	-
- 	Verificação da validade do número 		12345 	0 	-
- 	(Número válido) 		12345 	0 	-
2 	Início do loop de inversão 		12345 	0 	-
2.1 	Cálculo do resto da divisão por 10 (mem) 		12345 	0 	5
2.2 	Atualização do número (Num //= 10) 		1234 	0 	5
2.3 	Multiplicação e adição (Num_inv) 		1234 	5 	5
3 	Próxima iteração 		1234 	5 	-
3.1 	Cálculo do resto da divisão por 10 (mem) 		1234 	5 	4
3.2 	Atualização do número (Num //= 10) 		123 	5 	4
3.3 	Multiplicação e adição (Num_inv) 		123 	54 	4
4 	Próxima iteração 		123 	54 	-
4.1 	Cálculo do resto da divisão por 10 (mem) 		123 	54 	3
4.2 	Atualização do número (Num //= 10) 		12 	54 	3
4.3 	Multiplicação e adição (Num_inv) 		12 	543 	3
5 	Próxima iteração 		12 	543 	-
5.1 	Cálculo do resto da divisão por 10 (mem) 		12 	543 	2
5.2 	Atualização do número (Num //= 10) 		1 	543 	2
5.3 	Multiplicação e adição (Num_inv) 		1 	5432 	2
6 	Próxima iteração 		1 	5432 	-
6.1 	Cálculo do resto da divisão por 10 (mem) 		1 	5432 	1
6.2 	Atualização do número (Num //= 10) 		0 	5432 	1
6.3 	Multiplicação e adição (Num_inv) 		0 	54321 	1
7 	Próxima iteração 		0 	54321 	-
7.1 	(Condição de saída do loop) 		0 	54321 	-
- 	Saída do Resultado 	O número 12345 após inverter os algarismos é 54321 	0 	54321 	-
0 comments on commit 890ef84
Please sign in to comment.
Footer
© 2024 GitHub, Inc.
Footer navigation

    Terms
    Privacy
    Security
    Status
    Docs
    Contact

Copied! 

Skip to content

    Pricing

Sign in
Sign up
Px1906 /
unifor
Public

Code
Issues
Pull requests
Actions
Projects
Security

    Insights

Commit
Update AD1.md

    main 

@Px1906
Px1906 committed Mar 20, 2024
1 parent 137fbe9 commit 890ef84
Showing 1 changed file with 2 additions and 2 deletions.

4 changes: 2 additions & 2 deletions 4
RLA/AD1.md

Curso: Engenharia da Computação
Disciplina: Raciocinio Lógico e ALgorítimo
Código/Turma: T998-21
Professor: Ricardo Carubbi
Data: 20/03
Aluno(a): Sergio de Paiva Ximenes Filho
Matrícula: 2410330

1a chamada (Sim/Não): preencha com a opção correta
2a chamada (Sim/Não): preencha com a opção correta

1a chamada (Sim/Não): sim
2a chamada (Sim/Não): não
Avaliação Diagnóstica 1
Normas e exigências

Avaliação diagnóstica (AD) consiste em exercícios ou projetos desenvolvidos em grupo ao longo da disciplina.
A primeira avaliação diagnóstica (AD1) será composta por exercícios e equivale a 30% da nota da primeira avaliação (AV1).

Segue abaixo a expressão para o cálculo da AV1, sendo sendo AF1 equivale a primeira avaliação formativa e AD1, a primeira avaliação diagnóstica.

A AD1 é formada pela entrega dos exercícios (EX1) na data prevista e apresentação (AP1) de um dos exercícios escolhido pelo professor. Segue abaixo a expressão para o cálculo da AD1.

A EX1 é avaliada mediante a correção dos exercícios, sendo a avaliação no intervalo de 0% (não atende a questão), 50% (atende parcialmente) e 100% (atende em sua totalidade). Por exemplo, se o exercício equivale a 2 pontos e sua correção atente parcialmente a questão, então sua avaliação deste exercício será 1 ponto.

A AP1 é avaliada mediante aos pré-requisitos de clareza, organização e domínio do conteúdo. Portanto, o aluno deve demonstrar um bom entendimento do algoritmo, explicando seus princípios fundamentais, seu propósito e como ele funciona passo a passo.

A avaliação da AP1 é apenas considerada no intervalo de 0% (não atende os pré-requisitos), 25% (pouco atende os pré-requisitos), 50% (atende de forma mediana os pré-requisitos), 75% (atende de forma razoável os pré-requisitos) e 100% (atende em a totalidade dos pré-requisitos). Por exemplo, se na apresentação do exercício, o aluno atenter de forma razoável a questão, então sua avaliação da apresentação será 7.5 pontos.
Datas

    Entrega da primeira avaliação formativa (AF1) composta pelas listas de exerciícios 1, 2 e 3: 21/03/24
    Entrega dos exercícios da primeira avaliação diagnóstica (EX1): 21/03/24
    Apresentação da primeira avaliação diagnóstica (AP1): 21/03/24

Lista de questões
Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis,
e

, implemente e teste um algoritmo para trocar os valores atribuídos a elas.
Descrição geral do algoritmo

    Guardar o valor original da variável 

em uma variável auxiliar
;
Atribuir à variável
o valor original da variável
;
Atribuir à variável
o valor original da variável , que está armazenado na variável auxiliar
.
Exibir os novos valores de
e

    .

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo TrocaValores
DECLARE A, B, Mem: float
INICIO
ESCREVA "Digite o valor de A"
LEIA A
ESCREVA "Digite o valor de B"
LEIA B
Mem = B
B = A
A = Mem
ESCREVA A, B
FIM_ALGORITMO

Teste de mesa
A 	B 	Mem = B 	B = A 	A = Mem 	Saida
10 	4 	4 	10 	4 	4, 10
Questão 2 - Contagem (1 ponto)

Dado um conjunto
de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem do número de alunos que foram aprovados no exame. Será considerado aprovado o aluno que tirar

50 ou maior (no intervalo de 0 a 100).
Descrição geral do algoritmo

    Obter o número de notas 

a serem processadas;
Inicializar a contagem
com zero;
Enquanto houver notas a serem processadas, fazer repetidamente:

    obter a próxima nota;
    se a nota for suficiente para passar no exame (

) então adicionar 1 (um) à contagem

    ;

Exibir a contagem

    (número total de aprovações).

Fluxograma 01

Fluxograma conforme descrição do algoritmo acima, usando o loop ENQUANTO.
Pseudocódigo 01 (1 ponto)

Algoritimo aprovação
DECLARE N_ver, N_aprov, N_notas, i: Int
	notas: Float
INICIO
N_aprov = 0 
ESCREVA "Digite a quanidade de notas para avaliar"
LEIA N_notas
ENQUANTO N_notas <= 0 REPITA
	ESCREVA "Digite uma quantidade válida"
	LEIA N_notas
PARA N_ver DE 1 ATÉ N_notas FAÇA [PASSO 1]
	ESCREVA "Insira a nota"
	LEIA nota
	SE nota >= 50 E nota <= 100
		N_aprov =+ 1
		N_ver =+ 1
	SENÃO
		N_ver =+ 1
	FIM_SE
FIM_PARA
ESCREVA "A quantidade de notas aprovadas foi", N_aprov
FIM_ALGORÍRIMO

Teste de mesa 01
Chat GPT
Iteração 	Ação 	Entrada/Saída 	N_aprov 	N_ver
	Inicialização das Variáveis 		0 	0
	Entrada do Número de Notas 	5 		
1 	Mensagem: "Insira a nota" 			
	Entrada: nota 	70 		
	Condição SE: 70 >= 50 e 70 <= 100 (verdadeiro) 			
	N_aprov += 1 		1 	1
	N_ver += 1 			1
2 	Mensagem: "Insira a nota" 			
	Entrada: nota 	30 		
	Condição SE: 30 >= 50 e 30 <= 100 (falso) 			
	N_ver += 1 			2
3 	Mensagem: "Insira a nota" 			
	Entrada: nota 	85 		
	Condição SE: 85 >= 50 e 85 <= 100 (verdadeiro) 			
	N_aprov += 1 		2 	3
	N_ver += 1 			3
4 	Mensagem: "Insira a nota" 			
	Entrada: nota 	95 		
	Condição SE: 95 >= 50 e 95 <= 100 (verdadeiro) 			
	N_aprov += 1 		3 	4
	N_ver += 1 			4
5 	Mensagem: "Insira a nota" 			
	Entrada: nota 	40 		
	Condição SE: 40 >= 50 e 40 <= 100 (falso) 			
	N_ver += 1 			5
- 	Saída de Resultados 			
- 	Mensagem: "A quantidade de notas aprovadas foi 3" 			
Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de
números, implemente e teste um algoritmo para calcular a soma desses números.
Aceite apenas

maior ou igual a zero.
Descrição geral do algoritmo

    Obter a quantidade de números 

a serem somados.
Inicializar a variável
com 0 (zero).
Enquanto menos do que
números tiverem sido somados, fazer repetidamente:

    obter o próximo número 

;
calcular a soma atual, adicionando o número

    obtido à soma mais recente;

Exibir a soma dos

    números

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo soma_de_valores
DECLARE num_somados, num_soma: Int
	num, soma: Float
INICIO
soma = 0
ESCREVA "Digite o número de elementos do conjunto que você quer somar"
LEIA num_soma
ENQUANTO num_soma <= 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA num_soma
FIM_ENQUANTO
PARA num_somados DE 1 até Num_soma [PASSO 1] FAÇA
	ESCREVA "Digite um número"
	LEIA num
	soma =+ num
FIM_PARA
ESCREVA "O valor da soma total é", soma
FIM_ALGORITMO

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	soma 	num_somados
- 	Inicialização das Variáveis 		0 	0
- 	Entrada do Número de Elementos a Somar 	7 		
1 	Mensagem: "Digite um número" 			
	Entrada: num 	0.5 		
	soma += num 		0.5 	
	num_somados += 1 			1
2 	Mensagem: "Digite um número" 			
	Entrada: num 	-1.25 		
	soma += num 		-0.75 	
	num_somados += 1 			2
3 	Mensagem: "Digite um número" 			
	Entrada: num 	2.75 		
	soma += num 		2 	
	num_somados += 1 			3
4 	Mensagem: "Digite um número" 			
	Entrada: num 	0 		
	soma += num 		2 	
	num_somados += 1 			4
5 	Mensagem: "Digite um número" 			
	Entrada: num 	-3.5 		
	soma += num 		-1.5 	
	num_somados += 1 			5
6 	Mensagem: "Digite um número" 			
	Entrada: num 	1.75 		
	soma += num 		0.25 	
	num_somados += 1 			6
7 	Mensagem: "Digite um número" 			
	Entrada: num 	-2.25 		
	soma += num 		-2 	
	num_somados += 1 			7
- 	Saída de Resultados 			
- 	Mensagem: "O valor da soma total é -2" 			
Questão 4 - Cálculo de uma série (1 ponto)

Dado um conjunto de

termos da série, implemente e teste um algoritmo para calcular o valor de S, conforme definido abaixo:

Descrição geral do algoritmo

    Obter o número de termos 

;
Inicializar a variável
com 0 (zero).
Iterar o valor de
na variável iniciando com 0 (zero), de acordo com as instruções abaixo:

    calcular o numerador na variável 

;
calcular o denominador na variável
;;
calcular o termo da série na variável
, onde
;
adicionar esse termo à variável

    .

Exibir o valor da série

    .

Fluxograma
Pseudocódigo (1 ponto)

Algoritmo soma_da_serie
DECLARE Num_termo, termo: Int
	S: Float
INICIO
S = 0
ESCREVA "Digite a quantidade de termos da série que você quer somar"
LEIA Num_termo // 3 
ENQUANTO Num_termo < 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA Num_termo
FIM_ENQUANTO
PARA termo DE 1 ATÉ Num_termo [PASSO 1] FAÇA
	S =+ (2 * termo - 1)/(2 * termo)
FIM_PARA
ESCREVA "O valor da soma de", Num_termo, "termo(s) da série é", S
FIM_ALGORITMO

Teste de mesa (0.25 ponto)
Chat GPT
Iteração 	Ação 	Entrada/Saída 	S
- 	Inicialização das Variáveis 		0
- 	Entrada do Número de Termos da Série 		
1 	Mensagem: "Digite a quantidade de termos da série" 		
	Entrada: Num_termo 		-3
			
2 	Verificação do Número de Termos 		
	Enquanto Num_termo < 0 FAÇA 		
	Mensagem: "Digite uma quantidade válida" 		
	Entrada: Num_termo 		
	FIM_ENQUANTO 		
			
- 	Saída de Resultados (Nenhum Cálculo Realizado) 		
- 	Mensagem: "O valor da soma de -3 termo(s) da série é" 		
	0 		
Questão 5 - Cálculo fatorial (2 pontos)

Dado um número
, implemente e teste um algoritmo para calcular o fatorial de (escrito como ), onde

.
Descrição geral do algoritmo

    Obter o número 

, onde
;
Inicializar a variável
com 1 (um) para armazenar o resultado do cálculo do fatorial;
Iterar o valor de
na variável , ou seja, executar vezes, as instruções abaixo:

    Incrementar o valor atual 

multiplicando pelo valor de

    ;

Exibir o resultado (

    ).

Fluxograma
Pseudocódigo (2 pontos)

Algoritmo fatorial
DECLARE fato, n_mult, n: Int
INICIO
n_mult = 0
ESCREVA "Digite o numero do fatorial que voce quer calcular"
LEIA n
ENQUANTO n < 0 FAÇA
	ESCREVA "Digite um fatorial válido"
	LEIA n
FIM_ENQUANTO
PARA n_mult DE 1 PARA n [PASSO 1] FAÇA
	n_mult =+ 1
	fato = fato * n_mult
FIM_PARA
ESCREVA "O valor do fatorial de", n, "é", fato 
FIM_ALGORITMO

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		0 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		-50 	
				
2 	Verificação da Validade do Número 			
	Mensagem: "Digite um fatorial válido" 			
	Entrada: n 		-50 	
				
- 	Saída do Resultado 			
- 	(nenhuma saída, pois o número não é válido) 			
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		1 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		1 	
				
2 	Verificação da Validade do Número 			
	(nenhuma ação necessária, 0 é válido) 			
				
- 	Saída do Resultado 			
- 	Mensagem: "O valor do fatorial de 0 é 1" 		1 	
Iteração 	Ação 	Entrada/Saída 	fato 	n_mult
- 	Inicialização das Variáveis 		1 	0
- 	Entrada do Número para o Cálculo do Fatorial 			
1 	Mensagem: "Digite o número do fatorial que você quer calcular" 			
	Entrada: n 		6 	
				
2 	Verificação da Validade do Número 			
	(nenhuma ação necessária, 6 é válido) 			
				
3 	Cálculo do Fatorial 			
	n_mult = 1 			1
	fato = fato * n_mult 		1 	1
				
4 	n_mult = 2 			2
	fato = fato * n_mult 		1 	2
				
5 	n_mult = 3 			3
	fato = fato * n_mult 		2 	3
				
6 	n_mult = 4 			4
	fato = fato * n_mult 		6 	4
				
7 	n_mult = 5 			5
	fato = fato * n_mult 		24 	5
				
8 	n_mult = 6 			6
	fato = fato * n_mult 		120 	6
				
- 	Saída do Resultado 			
- 	Mensagem: "O valor do fatorial de 6 é 720" 		720 	
Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os
primeiros termos da sequência de Fibonacci, onde .
Os primeiros termos são:

. Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.
Descrição geral do algoritmo

    Obter o número de termos 

, onde
;
Inicializar os dois primeiros termos da série nas variável
e
com 0 (zero);
Iterar o valor de
, ou seja, executar vezes, as instruções abaixo:

    Imprimir o termo inicial 

(instrução para exibir a sequência ao atualizar a variável
);
Somar os termos
e na variável
;
Atribuir a variável
o valor da variável
;
Atribuir a variável
o valor da variável

        .

Fluxograma
Pseudocódigo (2 pontos)

Algoritimo fibonacci
DECLARE T1, T2, Tmem, TS, i: Int
INICIO
T1 = 0
T2 = 1
ESCREVA "Digite qual termo de fibonacci você quer calcular"
LEIA TS
ENQUANTO TS <= 0 FAÇA
	ESCREVA "Digite um termo válido"
	LEIA TS
FIM_ENQUANTO
PARA i DE 1 ATÉ TS [PASSO 1] FAÇA
	ESRCREVA T1
	Tmem = T1 + T2
	T1 = T2
	T2 = Tmem
FIM_PARA
FIM_ALGORITIMO

Teste de mesa
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					5
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					5
						
2 	Verificação da Validade do Número 					
	(nenhuma ação necessária, 5 é válido) 					
						
3 	Cálculo do Termo de Fibonacci 					
	PARA i DE 1 ATÉ 5 [PASSO 1] FAÇA 					
						
4 	i = 1 					
	Escreva: T1 		0 	1 		
						
	Tmem = T1 + T2 				1 	
	T1 = T2 		1 			
	T2 = Tmem 			1 		
						
5 	i = 2 					
	Escreva: T1 		1 	1 		
						
	Tmem = T1 + T2 				2 	
	T1 = T2 		1 			
	T2 = Tmem 			2 		
						
6 	i = 3 					
	Escreva: T1 		1 	2 		
						
	Tmem = T1 + T2 				3 	
	T1 = T2 		2 			
	T2 = Tmem 			3 		
						
7 	i = 4 					
	Escreva: T1 		2 	3 		
						
	Tmem = T1 + T2 				5 	
	T1 = T2 		3 			
	T2 = Tmem 			5 		
						
8 	i = 5 					
	Escreva: T1 		3 	5 		
						
	Tmem = T1 + T2 				8 	
	T1 = T2 		5 			
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					0
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					0
						
2 	Verificação da Validade do Número 					
	Mensagem: "Digite um termo válido" 					
	(Loop de entrada será repetido até que um número válido seja dado) 					
						
Iteração 	Ação 	Entrada/Saída 	T1 	T2 	Tmem 	TS
- 	Inicialização das Variáveis 		0 	1 		
- 	Entrada do Termo de Fibonacci a ser calculado 					-90
1 	Mensagem: "Digite qual termo de Fibonacci você quer calcular" 					
	Entrada: TS 					-90
						
2 	Verificação da Validade do Número 					
	Mensagem: "Digite um termo válido" 					
	(Loop de entrada será repetido até que um número válido seja dado) 					
						
Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Implemente e teste um algoritmo para inverter a ordem dos dígitos de um número inteiro positivo.
Descrição geral do algoritmo

    Obter o número inteiro positivo 

a ser invertido;
Inicializar a variável
com 0 (zero);
Enquanto o número for maior que zero (
), faça repetidamente:

    Calcular o último dígito do número na variável 

;
Adicionar o dígito ao número invertido
;
Remover o último dígito do número original

        ;
    Exibir o número invertido.

Fluxograma
Pseudocódigo (2 pontos)

Algoritimo Inver
DECLARE Num, Num_inv, mem, mem2: Int
INICIO
ESCREVA "Digite o número que voce quer inverter"
LEIA Num
mem2 = Num
ENQUANTO Num <= 9 FAÇA
	ESCREVA "O número precisa ser positivo e ter mais de dois algarismos"
	ESCREVA "Digite o número que voce quer inverter"
FIM_ENQUANTO
ENQUANTO Num > 0 FAÇA
	mem = Num % 10
        Num =// 10
	Num_inv =* 10
	Num_inv =+ mem
FIM_ENQUANTO
ESCREVA "O número", mem2, "após inverter os algarismos é", Num_inv
FIM_ALGORITIMO 

Teste de mesa
Chat GPT
Iteração 	Ação 	Entrada/Saída 	Num 	Num_inv 	mem
- 	Inicialização 		12345 	0 	-
1 	Leitura do número a ser invertido 		12345 	0 	-
- 	Verificação da validade do número 		12345 	0 	-
- 	(Número válido) 		12345 	0 	-
2 	Início do loop de inversão 		12345 	0 	-
2.1 	Cálculo do resto da divisão por 10 (mem) 		12345 	0 	5
2.2 	Atualização do número (Num //= 10) 		1234 	0 	5
2.3 	Multiplicação e adição (Num_inv) 		1234 	5 	5
3 	Próxima iteração 		1234 	5 	-
3.1 	Cálculo do resto da divisão por 10 (mem) 		1234 	5 	4
3.2 	Atualização do número (Num //= 10) 		123 	5 	4
3.3 	Multiplicação e adição (Num_inv) 		123 	54 	4
4 	Próxima iteração 		123 	54 	-
4.1 	Cálculo do resto da divisão por 10 (mem) 		123 	54 	3
4.2 	Atualização do número (Num //= 10) 		12 	54 	3
4.3 	Multiplicação e adição (Num_inv) 		12 	543 	3
5 	Próxima iteração 		12 	543 	-
5.1 	Cálculo do resto da divisão por 10 (mem) 		12 	543 	2
5.2 	Atualização do número (Num //= 10) 		1 	543 	2
5.3 	Multiplicação e adição (Num_inv) 		1 	5432 	2
6 	Próxima iteração 		1 	5432 	-
6.1 	Cálculo do resto da divisão por 10 (mem) 		1 	5432 	1
6.2 	Atualização do número (Num //= 10) 		0 	5432 	1
6.3 	Multiplicação e adição (Num_inv) 		0 	54321 	1
7 	Próxima iteração 		0 	54321 	-
7.1 	(Condição de saída do loop) 		0 	54321 	-
- 	Saída do Resultado 	O número 12345 após inverter os algarismos é 54321 	0 	54321 	-
0 comments on commit 890ef84
Please sign in to comment.
Footer
© 2024 GitHub, Inc.
Footer navigation

    Terms
    Privacy
    Security
    Status
    Docs
    Contact

Copied! 
