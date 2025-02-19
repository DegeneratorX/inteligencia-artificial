## Questão 1: Monty Hall Problem

Em um programa de televisão o participante é convidado a escolher entre três portas e atrás de uma delas encontra-se um prêmio (por exemplo, um carro). Após a escolha do participante, o apresentador abre uma das portas restantes e esta, obviamente, não contém o prêmio. A seguir, o apresentador oferece ao participante a opção de trocar a porta que escolheu pela outra porta restante. Qual deve ser a escolha do participante para que a sua chance de ganhar seja maximizada?

---

## Questão 2

Considere a seguinte rede Bayesiana:

- $A \rightarrow B$
- $A \rightarrow C$


Onde:

- $P(A) = 0.5$
- $P(B | A) = P(B | \neg A) = 0.2$
- $P(C | A) = 0.8$
- $P(C | \neg A) = 0.4$

Calcule:

a) $P(B)$  
b) $P(B | C)$  
c) $P(C | B)$  

---

## Questão 3

Considere a seguinte rede Bayesiana:

- $A \rightarrow B$
- $A \rightarrow C$
- $A \rightarrow D$

Onde:

- $P(A) = 0.5$
- $P(B | A) = P(C | A) = P(D | A) = 0.2$
- $P(B | \neg A) = P(C | \neg A) = P(D | \neg A) = 0.6$

Calcule:

a) $P(C | B, A)$  
b) $P(A | B, C, D)$  
c) $P(C | B)$  

---

## Questão 4

Considere a seguinte rede Bayesiana.

- $N \rightarrow S$
- $N \rightarrow C$
- $S \rightarrow M$
- $C \rightarrow M$

Verifique se (selecione entre V ou F):

a) $ S \perp N $  
b) $ S \perp C $  
c) $ S \perp C \mid N $  
d) $ S \perp C \mid M $  
e) $ S \perp C \mid M, N $  

---

## Questão 5
Seja a seguinte rede:

- $A \rightarrow B$
- $A \rightarrow C$
- $A \rightarrow E$
- $B \rightarrow E$
- $C \rightarrow E$
- $D \rightarrow C$

Determine:

a) O número de parâmetros necessários para especificar a distribuição conjunta de 5 variáveis binárias.

b) Assumindo que a relação entre as variáveis é dada pela rede Bayesiana abaixo, determine o número de parâmetros necessários para especificar a distribuição conjunta das 5 variáveis.

---

## Questão 6

Considere um conjunto de variáveis utilizadas para modelar um problema utilizando uma rede Bayesiana. A rede Bayesiana deve modelar uma situação onde um motorista tem a opção de voltar para casa após uma festa onde este pode ter ingerido bebida alcoólica. As variáveis em questão são as seguintes:

- **Bêbado** – Variável binária (bêbado ou não)  
- **Chovendo** – Variável binária (Está chovendo ou não)  
- **Preso** – Variável binária (O motorista será preso ou não)  
- **Falha nos freios** – Variável binária (irá ocorrer falha nos freios)  
- **Acidente** – Variável binária (O motorista provocará um acidente ou não)  
- **Gravidade do acidente** – Três níveis (leve, moderado e grave)  

Apresente uma proposta de estrutura para uma **rede Bayesiana** e determine o número de **parâmetros necessários** para especificar a probabilidade conjunta de todas as variáveis.

---

## Questão 7

Considere as seguintes redes Bayesianas desenvolvidas com o objetivo de modelar o problema de diagnóstico de **câncer no pulmão**.

#### Rede 1:

- $S \rightarrow C$
- $S \rightarrow L$
- $L \rightarrow C$
- $L \rightarrow B$

#### Rede 2:

- $S \rightarrow L$
- $B \rightarrow L$
- $C \rightarrow L$

#### Rede 3:

- $B \rightarrow S$
- $B \rightarrow L$
- $C \rightarrow L$
- $L \rightarrow S$

Nas figuras apresentadas, as variáveis são:

- $ S $ – **Fumante** (sim ou não)  
- $ L $ – **Tem Câncer** (sim ou não)  
- $ B $ – **Resultado da biópsia** (positivo ou negativo)  
- $ C $ – **Tem tosse** (sim ou não)  

a) Das opções listadas, qual apresenta a **melhor modelagem** do problema em questão?  
b) Qual modelo proposto apresenta o **menor número de parâmetros**?

## Questão 8

Considere a rede Bayesiana a seguir, utilizada para modelar uma situação de eleição. As variáveis são:

- $ I $ – **Inteligente**  
- $ H $ – **Honesto**  
- $ P $ – **Popular**  
- $ E $ – **Eleito**  
- $ L $ – **Muito dinheiro para campanha** (*Lots of Campaign Funds*)  

#### Rede:

- $I \rightarrow P$
- $H \rightarrow P$
- $H \rightarrow L$
- $L \rightarrow P$
- $P \rightarrow E$

#### $P(I)$
| $I$  | $P(I)$ |
|------|------|
| T    | 0.5  |
| F    | 0.5  |

#### $P(H)$
| $H$  | $P(H)$ |
|------|------|
| T    | 0.1  |
| F    | 0.9  |

#### $P(L | H)$
| $H$  | $P(L)$ |
|------|------|
| T    | 0.3  |
| F    | 0.9  |

#### Probabilidade condicional de $P(P | I, H, L)$

| $I$  | $H$  | $L$  | $P(P)$ |
|------|------|------|------|
| T    | T    | T    | 0.9  |
| T    | T    | F    | 0.4  |
| T    | F    | T    | 0.8  |
| T    | F    | F    | 0.2  |
| F    | T    | T    | 0.8  |
| F    | T    | F    | 0.3  |
| F    | F    | T    | 0.8  |
| F    | F    | F    | 0.1  |

#### Probabilidade condicional de $P(E | P)$

| $P$  | $P(E)$ |
|------|------|
| T    | 0.6  |
| F    | 0.1  |


### a) Verifique se as seguintes expressões são verdadeiras, de acordo com a rede apresentada:

- $ P(I | L) = P(I) P(L) $  
- $ P(E | P, L) = P(E | P, L, H) $  
- $ P(P | I, H) \neq P(P | I, H, L) $  

### b) Cálculo de Probabilidade

Calcule a **probabilidade** de alguém ser **inteligente**, dado que é **honesto**, teve **pouco dinheiro para campanha** e foi **eleito**:

## Questão 9

Três times de futebol, $A$, $B$ e $C$, jogam um contra o outro. Cada jogo tem três resultados possíveis: **vitória de cada time** e **empate**. 

Cada time tem um **nível fixo de qualidade** (número inteiro de 0 a 3), e este nível influencia probabilisticamente o **resultado da partida**.

### a) Estrutura da Rede Bayesiana

Projete uma estrutura de uma **rede Bayesiana** para modelar o problema. O modelo deve **incorporar o resultado dos três jogos**: 

- $AxB$ (Jogo entre $A$ e $B$)  
- $AxC$ (Jogo entre $A$ e $C$)  
- $BxC$ (Jogo entre $B$ e $C$)  

### b) Tabelas de Probabilidades Condicionais

Apresente possíveis **tabelas de probabilidades condicionais** para o problema.
