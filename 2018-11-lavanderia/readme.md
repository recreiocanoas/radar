#### CRRC Radar 2018

# Lavanderia Recreio das Canoas

[http://recreiocanoas.dyndns.tv:8123](http://recreiocanoas.dyndns.tv:8123 "Recreio Canoas IoT")  
(login e senha disponíveis na administração)  

Como começar a usar: [Guia do usuário](https://github.com/recreiocanoas/radar/blob/master/2018-11-lavanderia/guia_usuario.md "Guia do Usuário")

## Descrição sumária

A lavanderia do condomínio Recreio das Canoas, utilizada por muitos condôminos, disponibiliza máquinas de lavagem e secagem de roupas, mediante a compra de fichas.

Além de economizar valioso espaço em nossos compactos apartamentos, a  lavanderia dispõe de processo eficiente, com equipamentos com capacidade de 10 Kg por lavagem, permitindo redução do consumo de água e de produtos químicos descartados na natureza.

Seguem algumas características da lavanderia:

- O condomínio paga ao fornecedor um custo mensal, proporcional à quantidade de equipamentos alocados.
- Atualmente estão sendo alugadas pelo condomínio 2 máquinas de lavar e 2 máquinas de secar.
- O ciclo de uma lavagem dura 45 minutos e o de secagem 90 minutos em média.
- O horário de funcionamento da lavanderia é de 6 até 23 horas.

Multiplicando-se os equipamentos disponíveis pela quantidade de horas de funcionamento, concluímos que temos à disposição dos condôminos os seguintes totais de serviços de lavanderia:

- xx horas de lavagem (confirmar os dados)
- yy horas de secagem

Ocorre que há horários de congestionamento na lavanderia, em que chegam mais condôminos do que permite a capacidade  da lavanderia. Nesse caso, cria-se uma fila informalmente administrada pelos condôminos. 

Este projeto pretende criar condições para se otimizar a utilização da lavanderia do condomínio Recreio das Canoas. Com isso, espera-se evitar as filas e melhorar a experiência dos condôminos na utilização dos serviços de lavagem e secagem de roupa.

### Diagrama do Conflito

Para se estabelecer a linha de ação do projeto, é vital se estabelecer um diagrama que permite a análise detalhada do conflito. Para que essa estratégia funcione, é preciso que sejam identificados um objetivo e dois requisitos que possuam pré-requisitos conflitantes, como mostra a figura a seguir:

![Diagrama do Conflito](https://i.imgur.com/HO7bWxJ.png)

No caso da lavanderia do Recreio das Canoas, podemos identificar o conflito descrito abaixo:

| **CONFLITO**     | **Nome**         | **Descrição**          |  
| :---             |     :---:        |          :---:         |  
| Objetivo         | **Lavanderia eficiente** |  Deseja-se um bom serviço a custos razoáveis. |
| Requisito 1      | **Baixo custo** | Condomínio deve economizar no custo fixo.  |  
| Pré 1            | **Alugar poucas máquinas** |  Minimizar a quantidade de equipamentos alugados. |  
| Requisito 2      | **Alta disponibilidade**  |  Condômino deve dispor de máquinas livres para uso. |  
| Pré 2            | **Alugar muitas máquinas** |  Evitar filas, colocando mais equipamentos à disposição. |   

Uma breve análise das setas que interligam os elementos permite identificar possíveis pontos fracos no conflito:
 
| **ANÁLISE**      | **Nome**         | **Descrição**          |  
| :---             |     :---:        |          :---:         |   
| r1               | **Redução de custos** |  É uma preocupação legítima que deve ser considerada.  |
| p1               | **Contrato do fornecedor** |  A fórmula do custo está prevista no serviço contratado. | 
| r2               | **Máquinas livres** |  Deseja-se que o condômino disponha de máquinas livres. | 
| p2               | **Alugar mais é solução?** |  Buscar alternativas para maior disponibilidade. | 
| c                | **Mais ou menos máquinas** |  Conflito real, impossível aumentar e diminuir ao mesmo tempo. | 

- A seta `r1` indica que o serviço da lavanderia deve ser econômico, ou seja, essa é uma seta forte que mostra uma preocupação legítima que deve ser considerada.
- A seta `p1` representa a relação entre custo e a quantidade de máquinas, regidas pelo contrato com o fornecedor. Sempre se pode negociar redução de custos ou até mudança do fornecedor mas é normal esperar custos de acordo com a quantidade de equipamentos alocados para o condomínio.
- A seta `r2` indica que o serviço da lavanderia deve estar disponível para o condômino, ou seja, de nada nos adiantaria um serviço congestionado com filas enormes e desgastantes.
- O ponto fraco do conflito da lavanderia é a seta `p2`, pois pode-se tentar aumentar a disponibilidade sem aumentar a quantidade de equipamentos. Para isso, seria necessário um melhor aproveitamento do tempo total disponível.

De fato, observa-se muitas horas, principalmente à noite, em que a lavanderia está vazia. Não há notícia de alguma medição já realizada pela administração. Um dos objetivos deste projeto seria viabilizar uma medição que permitisse analisar o uso da lavanderia pelos condôminos ao longo da semana. Nesse contexto, seria bastante útil algum mecanismo que permitisse aos moradores identificar o melhor momento de utilizar a lavanderia, de acordo com as  possibilidades de cada um.

A ideia principal do projeto é utilizar o celular para saber se há máquinas de lavar/secar livres, sem que seja necessário o deslocamento até a lavanderia. Para isso, será instalado um dispositivo **IoT-Home-L1**, capaz de detectar e informar, através de um link público, detalhes sobre o ambiente da lavanderia.

Leva-se em consideração a existência de um sensor de presença, já existente na lavanderia, que acende a luz automaticamente na presença de alguém. Em um primeiro momento, a luz apagada por "algum tempo" deverá ser um indicador de lavanderia vazia. Assim, basta o condômino acompanhar de casa a utilização e descer assim que identificar uma pausa prolongada com a luz apagada.

Será isso suficiente para otimizar o uso da lavanderia do condomínio Recreio Canoas? Pode-se ainda, caso o projeto se mostre promissor, identificar individualmente os equipamentos ligados, de forma automática. Para isso, o dispositivo **IoT-Home-L1** teria que receber o sinal de sensores acoplados às respectivas tomadas de equipamentos. Mas essa seria uma segunda fase do projeto.

## IoT-Home-L1

O equipamento IoT-Home-L1, mostrado abaixo, possui um micro-computador ligado à Internet e é equipado com sensores de temperatura, umidade e luz. 

![IoT-Home-L1](https://i.imgur.com/729O3BN.png)

A tela de consulta é mostrada a seguir, onde se destacam as informações de iluminância indicando se a luz está acesa ou apagada. Como pode ser visto, outras informações são disponibilizadas como umidade, temperatura, posição do sol, além de informações sobre a performance do micro-computador e da rede de comunicação.

![](https://i.imgur.com/v8lXhGY.png)

Um painel de sinalização manual, vide à esquerda, poderá ainda ser operado, através da gentileza de qualquer condômino presente na lavanderia. Com isso, espera-se informar a todos a situação atualizada dos equipamentos da lavanderia:

- **AZUL - tudo livre**: ou seja todos os equipamentos da lavanderia estão livres!
- **VERDE - lavar & secar livres**: pelo menos uma máquina de lavar e uma máquina de secar estão livres.
- **AMARELO - lavar livre**: há pelo menos uma máquina de lavar livre, as secadoras estão todas ocupadas.
- **VERMELHO - nada livre**: todas as máquinas estão ocupadas.
- **DESLIGADO**: mesmo desligada a sinalização manual, o painel de iluminância ainda pode ser usado como informação. 

*Gostou? Me dá uma estrela :star:!*
