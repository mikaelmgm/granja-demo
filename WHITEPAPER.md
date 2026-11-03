# Happy Nugget · Whitepaper

Happy Nugget é um jogo idle de granja no tema Solana. As galinhas soltam pintinhos, a esteira leva até o abatedouro, eles viram **$NUGGET** e o caminhão vende a caixa. Quem entra ganha uma galinha de graça; o resto se compra com o token e com um pouco de SOL.

**Premissas das contas**

- Supply de 1 bilhão de $NUGGET, lançado na pump.fun.
- Market cap de lançamento entre 27k e 37k dólares. A base é 30k, com 20k, 40k e 50k ao lado.
- 1 SOL = 100 dólares. A 30k, 100.000 $NUGGET valem 3 dólares.
- O jogo foi medido para durar de 7 a 14 dias sem mudanças; os nerfs seguintes é que o fazem durar mais.

**A resposta curta**, numa simulação de 200 jogadores variados por 14 dias, a 30k:

| Perfil | Jogadores | Investe (mediana) | Recupera em (mediana) | Não recuperou em 14 dias |
| --- | --- | --- | --- | --- |
| Sardinha ativa | 59 | $12 | 7 dias | 18 |
| Sardinha parada | 52 | $13 | 14 dias | 24 |
| Médio | 75 | $60 | 5 dias | 3 |
| Baleia | 14 | $170 | 3 dias | 0 |

## Como o jogo funciona

**Galinha → pintinho → esteira → abatedouro → caixa → caminhão → saldo**

1. A galinha trabalha e solta pintinhos.
2. A esteira do celeiro leva os pintinhos até o abatedouro, até o limite dela por minuto.
3. O abatedouro transforma cada pintinho em 3,5 $NUGGET, vezes o nível dele.
4. Os nuggets ficam na caixa, que guarda 4 horas de produção. Cheia, as galinhas param.
5. O caminhão leva a caixa e a venda é na hora: 10% ficam de frete, que é queimado.

Os gargalos são de propósito. Cada esteira dá conta de um celeiro cheio de galinhas médias; quem tira galinha boa enche a esteira e é empurrado para o próximo celeiro. A caixa pequena cobra de quem não entra: ou ele volta mais vezes, ou compra caixa maior.

**Raridades** (o ovo sorteia a raridade; a produção é sorteada dentro da faixa)

| Raridade | Chance no ovo | Pintinhos por minuto | Trabalha até cansar |
| --- | --- | --- | --- |
| Comum | 50% | 1 a 6 | 1 h 20 min |
| Incomum | 28% | 6 a 12 | 1 h 40 min |
| Rara | 14% | 12 a 20 | 2 h |
| Épica | 6% | 30 a 50 | 2 h 20 min |
| Lendária | 1,96% | 90 a 140 | 2 h 50 min |
| Mítica | 0,04% | 300 a 450 | 3 h 20 min |

## Celeiros, sono e galo

| Celeiro | Como abre | Esteira | Descanso completo | Produção |
| --- | --- | --- | --- | --- |
| 1 · Madeira | Grátis | 60 por minuto | 1 h 40 min | base |
| 2 · Pedra | 11ª galinha, 12 h de obra | 100 | 1 h 7 min | +8% |
| 3 · Metal | 21ª galinha, 24 h de obra | 200 | 40 min | +16% |
| 4 · Diamante | 31ª galinha + 0,1 SOL, na hora | 500 | 25 min | +30% |

**Quantas galinhas enchem a esteira.** A galinha não trabalha o tempo todo, porque dorme; a média que sai do ovo solta de 6 a 9 pintinhos por minuto, conforme a cama. Sem galo / com galo:

| Celeiro | Esteira | Galinhas médias | Raras | Épicas | Lendárias |
| --- | --- | --- | --- | --- | --- |
| 1 · Madeira | 60 | 10 / 8 | 7 / 5 | 3 / 2 | 1 |
| 2 · Pedra | 100 | 14 / 11 | 10 / 8 | 4 / 3 | 1 |
| 3 · Metal | 200 | 24 / 21 | 17 / 15 | 6 | 2 |
| 4 · Diamante | 500 | 54 / 49 | 38 / 35 | 15 / 14 | 5 |

A esteira de Madeira era de 30 e enchia com 5 galinhas médias: da 6ª em diante, a galinha comprada não rendia nada. Isso travava o médio e não a sardinha de 3 galinhas, e por isso a sardinha recuperava mais rápido que o médio. Com 60, ela enche com o celeiro cheio.

**Sono:** trabalhando, a energia cai de 100% a 0% e ela dorme, sem produzir. Sem galo, dorme até 100%, ou você toca em Acordar depois de 50%. Com galo, acorda sozinha em 50%. Cansada ou dormindo, não troca de celeiro.

**O galo está roubado?** Medimos com 120 jogos por perfil, com e sem galo:

| Perfil | Sem galo, por dia | Com galo | Ganho |
| --- | --- | --- | --- |
| Sardinha de 5 galinhas, entra a cada 4 h | 77 mil | 98 mil | +27% |
| Médio de 10 galinhas, a cada 4 h | 135 mil | 157 mil | +16% |
| Médio de 20 galinhas, a cada 4 h | 494 mil | 546 mil | +11% |
| Médio de 20 galinhas, a cada 8 h, caixa de 10 h | 465 mil | 537 mil | +16% |
| Médio de 20 galinhas, a cada 8 h, caixa de 4 h | 319 mil | 312 mil | nada |
| Baleia de 40 galinhas, a cada 4 h | 1,60 mi | 1,78 mi | +11% |

Quem deixa a caixa encher não ganha nada com o galo: a caixa trava antes do sono. Foi por isso que o galo ficou barato e não ganhou buff. Mexer no sono ou no galo mudaria o ROI de todo mundo, e o problema está no preço.

O galo sai **só em SOL: 0,05 por 3 dias ou 0,1 por 7 dias** ($1,40 a $1,70 por dia). Para o médio de 20 galinhas que entra a cada 4 h, ele rende uns 52 mil $NUGGET por dia, $1,57 a 30k: o plano de 7 dias se paga por pouco. Para a baleia rende $5,40 por dia, e para a sardinha, uns 60 centavos, então não paga para ela. A 50k, rende o dobro em dólar e se paga para o médio com folga.

**Sujeira:** o celeiro leva 24 horas para chegar ao piso, onde rende 70%. Limpar é de graça, com um toque.

## Preços

O que se compra com **$NUGGET** é queimado. O que se compra com **SOL** vai inteiro para a carteira do dev, que paga a recompra do token e as atualizações.

Os bônus em porcentagem (horta, galo, açougue) foram precificados pelo jogador médio de 20 galinhas: custam um pouco menos do que rendem para ele. Por serem porcentagem, rendem muito para a baleia e não pagam para a sardinha.

**Em $NUGGET**

| Item | Preço | a 20k | a 30k | a 40k | a 50k |
| --- | --- | --- | --- | --- | --- |
| Ovo avulso | 110.000 | $2,20 | $3,30 | $4,40 | $5,50 |
| Ovo no pacote de 5 (cada) | 80.000 | $1,60 | $2,40 | $3,20 | $4,00 |
| Ovo no pacote de 10 (cada) | 55.000 | $1,10 | $1,65 | $2,20 | $2,75 |
| Pato (cerca de 2 h sem raposa) | 5.000 | $0,10 | $0,15 | $0,20 | $0,25 |
| Caixa de 6 h | 50.000 | $1,00 | $1,50 | $2,00 | $2,50 |
| Caixa de 10 h | 75.000 | $1,50 | $2,25 | $3,00 | $3,75 |
| Caixa de 16 h | 120.000 | $2,40 | $3,60 | $4,80 | $6,00 |
| Terminar a obra da Pedra | 90.000 | $1,80 | $2,70 | $3,60 | $4,50 |
| Terminar a obra do Metal | 180.000 | $3,60 | $5,40 | $7,20 | $9,00 |
| Chocar um ovo (12 h) | 30.000 | $0,60 | $0,90 | $1,20 | $1,50 |
| Vender um ovo (você recebe) | 15.000 | $0,30 | $0,45 | $0,60 | $0,75 |
| Fazendeiro (horta inteira, de vez) | 300.000 | $6,00 | $9,00 | $12,00 | $15,00 |
| Milho (+4% por 24 h) | 15.000 | $0,30 | $0,45 | $0,60 | $0,75 |
| Girassol (+6% por 24 h) | 22.000 | $0,44 | $0,66 | $0,88 | $1,10 |
| Frutas (+10% por 24 h) | 37.000 | $0,74 | $1,11 | $1,48 | $1,85 |
| Reforma de vagas (+2) | 35.000 a 130.000 | até $2,60 | até $3,90 | até $5,20 | até $6,50 |
| Fusão | em breve | | | | |

**Em SOL**

| Item | SOL | Dólares |
| --- | --- | --- |
| Galo por 3 dias | 0,05 | $5 |
| Galo por 7 dias | 0,1 | $10 |
| Caçador por 7 dias | 0,12 | $12 |
| Empresinha (1,15x por pintinho) | 0,1 | $10 |
| Indústria (1,3x) | 0,2 | $20 |
| Usina Nuclear (1,75x) | 0,3 | $30 |
| 4º celeiro, Diamante | 0,1 | $10 |

## Defesa

- **Raposa:** vem em média a cada 2 horas, escolhe um caminho e come os pintinhos da esteira por 40 minutos.
- **Pato (5.000 $NUGGET, até 6):** atrai uma raposa para a mata e é gasto. Cada pato protege por cerca de 2 horas, e 6 patos dão cerca de 12 horas. O jogo mostra isso na hora de comprar.
- **Ladrão:** só aparece com **mais de 10 galinhas** e mais de um celeiro, em média uma vez por dia. Sem caçador, ele leva uma galinha. Pato não engana ladrão.
- **Caçador (0,12 SOL por 7 dias):** acerta toda raposa e todo ladrão. Custa $1,71 por dia e salva, por dia:

| Perfil | Sem caçador | Com caçador | Galinhas no fim, sem / com |
| --- | --- | --- | --- |
| Médio de 15 galinhas | 214 mil | 301 mil | 10 / 16 |
| Médio de 20 galinhas | 321 mil | 468 mil | 11 / 21 |
| Baleia de 40 galinhas | 1,37 mi | 1,53 mi | 27 / 40 |

A 30k, ele salva de $2,60 a $4,70 por dia, então se paga para todo mundo acima de 10 galinhas. Sem ele, o ladrão leva galinhas até sobrarem umas 10.

## 200 jogadores simulados

Cada jogador foi jogado por 14 dias pelo próprio jogo, com sorteio de raridade, raposa, ladrão, sujeira, sono e caixa enchendo. O ROI conta o dia em que o que ele ganhou passa o que ele gastou até ali, incluindo o galo e o caçador renovados. O ovo foi cobrado pelo pacote que cada um compraria.

**Quem são**

- **Sardinhas (111):** de 1 a 5 ovos. Metade entra a cada 3 a 6 horas; a outra metade entra 1 ou 2 vezes por dia e quase nunca limpa. Algumas compram patos ou galo.
- **Médios (75):** de 8 a 25 ovos, entram a cada 2 a 12 horas. 60% contratam caçador, 45% galo, 40% compram mais ovos na 1ª semana, 30% compram caixa maior.
- **Baleias (14):** de 30 a 40 ovos, entram a cada 2 a 4 horas, com galo, caçador, patos, caixa grande, açougue melhorado, obras aceleradas e quase sempre o Diamante.

**Resultado a 30k**

| Perfil | ROI, 25% mais rápidos | Mediana | 25% mais lentos | Lucro em 14 dias (mediana) | Os 10% melhores | Galinhas no fim |
| --- | --- | --- | --- | --- | --- | --- |
| Sardinha ativa | 5 dias | 7 | não pagou | $10 | $51 | 4 |
| Sardinha parada | 9 dias | 14 | não pagou | $0 | $15 | 4 |
| Médio | 4 dias | 5 | 7 | $78 | $222 | 15 |
| Baleia | 3 dias | 3 | 4 | $664 | $1.161 | 35 |

**ROI mediano por market cap** (só de quem recuperou em 14 dias)

| Perfil | a 20k | a 30k | a 40k | a 50k |
| --- | --- | --- | --- | --- |
| Sardinha ativa | 6 dias | 6 | 6 | 6 |
| Sardinha parada | 10 dias | 10 | 10 | 10 |
| Médio | 5 dias | 5 | 5 | 5 |
| Baleia | 4 dias | 3 | 3 | 2 |

Quem só gasta token tem o mesmo ROI em qualquer market cap: gasto e ganho sobem juntos. O SOL pesa mais com o token barato, por isso quem compra galo, caçador e açougue recupera mais devagar a 20k.

**O sortudo:** 33 dos 200 tiraram pelo menos uma Lendária. Entre eles, o ROI mediano foi de 3 dias para a sardinha ativa, 4 para o médio e 2 para a baleia. Uma Lendária sozinha enche a esteira de Madeira, então o prêmio de sorte cresce quando ela vai para um celeiro melhor.

**Mais de 10 mil jogos.** Antes de chegar nestes números, testamos 12 variantes de regras com a mesma população, cada uma recalibrada para o médio recuperar em 4 a 5 dias. O que cada regra come da produção (sem a regra, quanto o jogador ganharia a mais):

| Regra | Sardinha ativa | Médio |
| --- | --- | --- |
| Esteira de Madeira em 30 | +33% | +61% |
| Sono | +31% | +15% |
| Caixa de 4 h | +3% | +16% |
| Ladrão | quase nada | +10% |
| Sujeira | +1% | +2% |
| Raposa | quase nada | quase nada |

Tirar o sono deixava a sardinha mais rápida (3 dias), porque é ele que mais pesa na granja pequena. A esteira em 30 era o que invertia a ordem. Sem mexer nela, nenhuma escada de preço do ovo deixava a sardinha ativa acima de 6 dias.

## Emissão de token: o ponto mais importante

Nos 14 dias, os 200 jogadores tiraram **902 milhões de $NUGGET**, quase o supply inteiro. Voltaram para a queima 272 milhões (ovos, caixas, patos, frete), e a carteira do dev recebeu 35 SOL ($3.500).

| | $NUGGET | Em dólares a 30k |
| --- | --- | --- |
| Pago aos jogadores | 902 mi | $27.100 |
| Queimado | 272 mi | $8.200 |
| Emissão líquida | 631 mi | $18.900 |
| SOL para o dev | 35 SOL | $3.500 |

Isso vem direto da meta de ROI: se o jogador médio recupera em 5 a 6 dias, em 14 dias ele tira de 2 a 3 vezes o que gastou, e quase todo o gasto dele é em token. Com o SOL do dev, a recompra a 30k compra uns 115 milhões, um sexto do que sai.

Para fechar a conta, uma destas, ou uma mistura:

- **Um cofre de recompensas** com um teto por dia, dividido entre os jogadores pelo que produziram. O jogo continua igual, mas o $NUGGET do dia é uma fatia do cofre.
- **Nerf ao longo do tempo:** o abatedouro paga um pouco menos por pintinho a cada semana, ou a cada tantos jogadores.
- **Mais queima:** frete maior, ou ovo e obra mais caros. Isso também atrasa o ROI.
- **Market cap maior:** a 300k, os mesmos tokens valem 10 vezes mais em dólar e o mesmo SOL compra 10 vezes menos token. Nada disso muda a conta em token.

## Pontos em aberto

- **Sardinha com azar.** 30% das sardinhas ativas e 46% das paradas não recuperam em 14 dias: com 1 a 5 ovos, quem só tira Comum demora. É o preço de a sardinha não ser rápida.
- **Preços em centavos.** Pato, milho, chocar e vender ovo ficam abaixo de 1 dólar a 30k. Vem de cobrar pelo que rendem para o jogador médio.
- **O preço do SOL.** Todas as contas usam 100 dólares.
- **O que não entrou na simulação:** a horta, chocar ovos em vez de vender, a reforma de vagas e a fusão.
