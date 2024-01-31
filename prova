
# Uso de TAD - Fila de reprodução

Conforme definição em Bart, uma fila de reprodução é:

```C
Um componente que exibe uma lista de elementos que serão reproduzidos em ordem. O usuário pode controlar a reprodução da fila usando gestos ou botões. A fila de reprodução geralmente é usada para reproduzir conteúdo, como música, vídeos ou podcasts.
```

As funcionalidades associadas em uma fila de reprodução incluem:

- Adição de itens: o usuário pode adicionar itens à fila de reprodução.

- Remoção de itens: o usuário pode remover itens da fila de reprodução.

- Controle de reprodução: o usuário pode controlar a reprodução da fila de reprodução, seja para avançar, retroceder, pausar ou reproduzir.


Além dessas funcionalidades básicas, as filas de reprodução também podem incluir recursos mais avançados, como:

- Reprodução aleatória: o usuário pode reproduzir os itens da fila de reprodução em ordem aleatória.
- Repetição: o usuário pode repetir a reprodução de um item específico ou de toda a fila de reprodução.


Os elementos em uma fila de reprodução são organizados segundo uma política, que irá determinar a ordem de reprodução.

As políticas de organização mais comuns para filas de reprodução incluem:

- Ordem cronológica: os elementos são reproduzidos na ordem em que foram adicionados à fila.
- Ordem aleatória: os elementos são reproduzidos em ordem aleatória.
- Ordem de reprodução: os elementos são reproduzidos na ordem especificada pelo usuário.


Nesse trabalho você deverá implementar um TAD Fila de reprodução que tenha __no mínimo__ as seguintes interfaces:


- criar_fila_reproducao(): 
    - cria a fila de tamanho fixo
- adicionar_fila_reproducao(): 
    - adiciona um elemento a fila criada se ainda for possível
- avancar_fila_reproducao(k): 
    - avança o indicador da fila k posições
    - registra a movimentação _avancou k posicoes_
- retroceder_fila_reproducao(k): 
    - retrocede o indicador da fila k posições
    - registra a movimentação _retrocedeu k posicoes_
- pausar_fila_reproducao(): 
    - suspende a reprodução de um elemento
    - registra a ação _pausou a reproducao_
- reproduzir_fila_reproducao(): 
    - inicia ou retoma a reprodução de um elemento
    - registra a ação _iniciou(retomou) a reproducao_


O TAD fila de reprodução também deve permitir que seus itens sejam organizados conforme a:

- ordem _aleat_ ória
- ordem _crono_ lógica
- ordem de _repro_ dução

Ao instanciar a fila é preciso estabelecer qual será a ordem com que os elementos serão organizados. A criação da fila então será indicada por uma entrada similar ao exemplo abaixo:

```
10 aleat
```
uma fila de reprodução com 10 elementos organizados em ordem aleatória.



Para a reprodução em __ordem aleatória__ os elementos a serem acessados são definidos por deslocamentos (avanço e retrocesso). Esses deslocamentos devem considerar a posição atual. O comando a seguir

```
reproduzir 5
```

gera a seguinte interação:

```C
avancar_fila_reproducao(5);
reproduzir_fila_reproducao();
```

e o seguinte comando:

```
reproduzir -3
```

gera a seguinte interação

```C
retroceder_fila_reproducao(3);
reproduzir_fila_reproducao();
```


No caso da __ordem de reprodução__ as interações com a fila acontece somente atraves das interfaces citadas anteriormente, e precisa considerar que o valor informado para uma reprodução é a ordem do elemento. Por exemplo, considere que após inserir os elementos na fila de reprodução, o indicador da reprodução estará sempre posicionado no primeiro elemento, e o seguinte comando é informado:

```
avancar 5
reproduzir
```
a interação com a fila será de:

```C
avancar_filareproducao(4);
reproduzir_filareproducao();
```

em  seguinda o outro comando é informado como segue:

```
avancar 2
reproduzir
```

a interação com a fila será de:

```C
avancar_filareproducao(1);
reproduzir_filareproducao();
```

Quando o acesso da fila for feito na _ordem cronológica_ os eventos de movimentação são sempre com passo unitário. 

Assim uma fila de reprodução com cinco músicas, que já tenha reproduzido quatro de suas músicas, recebendo como entrada o seguinte comando

```
avancar
reproduzir
```

terá a seguinte interação com a fila:

```C
avancar_filareproducao(1);
reproduzir_filareproducao();
```

```
retroceder
reproduzir
```

terá a seguinte interação com a fila:

```C
retroceder_filareproducao(1);
reproduzir_filareproducao();
```
