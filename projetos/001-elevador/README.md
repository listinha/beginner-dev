# 001 - Elevador

Em um dos muitos universos paralelos, há um planeta tal como o nosso mas com uma diferença peculiar: eles tem prédios bem altos e os elevadores funcionam de uma forma um pouco diferente.
Apesar de diferentes, eles servem o mesmo propósito: levar as pessoas para o andar que elas desejam ir.

Um prédio neste universo pode facilmente ter mais de mil andares -- acima do chão -- e mais mil abaixo da terra! Não caberiam tantos botões nos elevadores. Por isto, ao invés de ter um botão para ir até cada andar, existem botões para subir ou descer um certo número de andares.

Por exemplo, um elevador pode ter dentro dele os botões `+1`, `+2`, `+50` como também alguns botões para descer: `-1`, `-2`, `-50`, `-600`.
Alguém que estiver no andar 80 e quiser ir para o andar 137, precisará pressionar os botões `+50`, `+2`, `+2`, `+2` e `+1`. A ordem que os botões forem pressionados não importa: ela subirá 57 andares de qualquer jeito. E se ela quiser, também poderá, ao invés de pressionar o botão `+2`, pressionar duas vezes o botão `+1`. Ou se ela estiver em um dia um pouco louco, pode também pressionar `+2`, `-2` e `+2` para subir 2 andares.

### O problema

Você foi contratado para fazer um programa que, dado uma sequência de botões apertados e um andar inicial, diga quantas paradas o elevador fez e em qual andar ele se encontra em cada parada.

Seu programa deve ler um arquivo de texto chamado `elevador.txt`. Neste arquivo, haverá diversas entradas para seu programa solucionar. Cada entrada é independente uma da outra e seu programa deve solucioná-las de forma independente.

Uma entrada consiste em três números separados por espaço: o andar inicial em que o elevador se encontra, a quantidade de andares abaixo da terra e a quantidade de andares existentes acima da terra.
Em uma linha nova há os botões que foram pressionados, sempre com o prefixo `+` ou `-`. Os números são separados por espaços.

Um exemplo de entrada para o arquivo elevador.txt:

```
329 100 400
-2 -2 -5 -300 -50 +300 +1
```

Neste caso, o elevador possui um total de 501 andares: 100 abaixo da terra, 400 acima e o térreo. Ele se encontra atualmente no andar 329 acima da terra.
Ele parou então nos andares 327, 325, 320, 20, -30, 270 e 271.

Para cada parada que o elevador faz, seu programa deve imprmir uma linha contendo dois números separados por espaço: o número da parada que o elevador fez (a começar por 1) e o andar em que ele se encontra. Para o exemplo acima, a saída do programa deverá ser:

```
1 327
2 325
3 320
4 20
5 -30
6 270
7 271
```

Seu programa não deverá imprimir nada além desta saída.

### Exemplos

Para a seguinte entrada:

```
0 50 50
+50 +5 -100
90 200 20
-100
```

Seu programa deverá imprimir:

```
1 50
2 50
3 -50
1 -10
```

Note que há dois elevadores, independentes um do outro. Você não deve imprimir nenhum separados entre um elevador e outro, mas simplesmente deve reiniciar a contagem da parada que o elevador fez. Note também que quando o elevador foi instruído a subir além do andar mais alto do prédio, ele simplesmente permaneceu no último andar.

### Notas

- O elevador nunca passa dos limites. Se alguém tentar ir para um andar maior do que o prédio, o elevador simplesmente vai para o último andar. O mesmo ocorre se alguém tentar ir para um andar negativo que ultrapassa os limites do fundo do prédio.
- O elevador faz uma parada para cada botão pressionado. Isto é, se os botões `+2`, `+2` e `+1` forem pressionados a partir do andar térreo (zero), o elevador irá parar nos andares 2, 4 e 5.