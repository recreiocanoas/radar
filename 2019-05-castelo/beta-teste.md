#### CRRC Radar 2018

# Projeto Água do Castelo

#### Instalação de sensor de nível de água em tempo real no reservatório do Castelo.

## Medições

Medições realizadas no Castelo indicam que a parte útil da caixa d'água tem uma altura média estimada em 2.91 metros. A seguir estão indicadas as demais medidas do castelo: 

![](https://i.imgur.com/2mHKGsF.png)

A base do sensor ToF, de onde se iniciam a contagem das medidas de distância, está localizado a 15 cm de altura, contados a partir da borda superior do reservatório.

Sendo assim, temos as seguintes medidas extremas quando a caixa estiver cheia e vazia:

- Reservatório cheio: o sensor deverá medir  150 mm;
- Reservatório vazio: o sensor deverá medir 3006 mm = 150 + 2910 mm;

Internamente, temos um reservatório cilíndrico circular fechado, parecido com uma fôrma de bolo. O acesso se dá exclusivamente por uma escada embaixo do reservatório, localizada no centro da forma. Como mostra a foto abaixo, o nível da água pode ser visto do topo da escada.

![Reservatório](https://i.imgur.com/1AcOmRi.png)

## Resultados

Seguem abaixo algumas das informações obtidas com a entrada em beta-teste do sensor de nível de água em tempo real no reservatório do Castelo.

### Painel em tempo real

A partir deste painel, a coluna da esquerda indica a percentagem existente do volume de água, além da altura da linha d'água. A coluna central monitora  a temperatura e umidade no interior do sensor, a iluminância no interior da caixa d'água, bem como a distância medida pelo sensor laser ToF (Time of Flight).
 
![](https://i.imgur.com/XxwDZus.png)

A coluna da direita monitora o computador utilizado no sensor, indicando dados de memória, uso de disco e da rede, além da temperatura do processador.

### Histórico

Pode-se obter gráficos do comportamento das medidas ao longo de 1 dia, 3 dias ou de 1 semana, como mostram as imagens obtidas a seguir:

#### 1 dia

Segue a descrição das medidas:

- A primeira medida é a distância medida do topo da caixa até a água. Pode-se avaliar a  quantidade de água na caixa observando-se a parte superior da curva, até atingir a marca de 3 metros aproximadamente;

- O segundo gráfico mostra as temperaturas interna do sensor e do GPU do computador;

- Os gráficos da terceira linha representam a umidade e uso do processador;
- O quarto gráfico indica a luminosidade no interior da caixa d'água e serve para alertar quando a lâmpada interna está acesa.
- Os gráficos da última linha indicam utilização de memória e da rede de dados que foi ligada no dia 8/8/2019.

![](https://i.imgur.com/IaiIsqt.png)

#### 3 dias

Pode-se obter dados de períodos de três dias, o que nos permite avaliar o comportamento do consumo de água por longos períodos.

![](https://i.imgur.com/TQ4kNdD.png)

#### 1 semana

Tendo em vista a análise do consumo, o gráfico do histórico semanal é bastante interessante. Esses são dados reais de nosso consumo na última semana e pode-se verificar que em diversos momentos, principalmente nos finais de semana a caixa chega a esvaziar quase que completamente. 

![](https://i.imgur.com/y6Ak995.png)

A entrada em operação deste sistema vai nos possibilitar o acompanhamento do  nosso consumo de água, hora a hora, dia a dia, de forma a estabelecer critérios para avaliação do sistema de fornecimento e embasar decisões futuras a respeito desse bem tão precioso que temos no condomínio Recreio das Canoas.