#### CRRC Radar 2018

# Lavanderia

## Descrição sumária

A lavanderia do condomínio Recreio das Canoas, utilizada por muitos condôminos, disponibiliza máquinas de lavagem e secagem de roupas, mediante a compra de fichas.

Além de economizar valioso espaço em nossos compactos apartamentos, a  lavanderia dispõe de processo eficiente, com equipamentos com capacidade de 10 Kg por lavagem, permitindo redução do consumo de água e de produtos químicos descartados na natureza.

Seguem algumas características da lavanderia:

- O condomínio paga custo mensal, proporcional à quantidade de equipamentos alocados.
- Atualmente há disponíveis 2 máquinas de lavar e 2 máquinas de secar.
- O ciclo de uma lavagem dura 45 minutos e o de secagem 90 minutos em média.
- O horário de funcionamento é de 6 até 23 horas.

Multiplicando-se os equipamentos disponíveis pela quantidade de horas de funcionamento, concluímos que temos à disposição dos condôminos os seguintes totais de serviços de lavanderia:

- xx horas de lavagem
- yy horas de secagem

Ocorre que há horários de congestionamento na lavanderia, em que chegam mais condôminos do que permite a capacidade instantânea da lavanderia. Nesse caso, estabelece-se uma fila que é informalmente administrada pelos condôminos. 

Este projeto pretende criar condições para se otimizar a utilização da lavanderia do condomínio Recreio das Canoas, evitando as filas e melhorando a experiência dos condôminos na utilização desses serviços.

### Diagrama do Conflito

Para se estabelecer a linha de ação do projeto, é vital se estabelecer um diagrama que permite a análise detalhada do conflito. Ele deve possuir um objetivo e dois requisitos que possuam pré-requisitos conflitantes, como mostra a figura a seguir:

![Diagrama do Conflito](https://i.imgur.com/HO7bWxJ.png)

No caso da lavanderia do Recreio das Canoas, podemos identificar o conflito descrito na tabela abaixo:

| **CONFLITO**     | **Nome**         | **Descrição**          |  
| :---             |     :---:        |          :---:         |  
| Objetivo         | **Lavanderia eficiente** |  Deseja-se um bom serviço a custos razoáveis. |
| Requisito 1      | **Baixo custo** | Condomínio deve pagar pouco custo fixo.  |  
| Pré 1            | **Alugar poucas máquinas** |  Minimizar a quantidade de equipamentos alugados. |  
| Requisito 2      | **Alta disponibilidade**  |  Condômino deve dispor de máquina livre para uso. |  
| Pré 2            | **Alugar muitas máquinas** |  Evitar filas, colocando mais equipamentos à disposição. |   

Uma breve análise das setas que interligam os elementos permite identificar possíveis pontos fracos no conflito:
 
| **ANÁLISE**      | **Nome**         | **Descrição**          |  
| :---             |     :---:        |          :---:         |   
| r1               | **Redução de custos** |  É uma preocupação legítima que deve ser considerada.  |
| p1               | **Contrato do fornecedor** |  O custo está previsto no serviço contratado. | 
| r2               | **Máquinas livres** |  Deseja-se que o condômino disponha de máquinas livres. | 
| p2               | **Alugar mais é solução?** |  Buscar alternativas para maior disponibilidade. | 
| c                | **Mais ou menos máquinas** |  Conflito real, impossível aumentar e diminuir ao mesmo tempo. | 

Levando-se em consideração que há muitas horas em que a lavanderia está vazia, irá ser implementado um mecanismo que permita aos moradores identificarem o melhor momento de utilizar a lavanderia, de acordo com as suas possibilidades.

A ideia principal do projeto é informar aos condôminos se as máquinas estão livres, sem que seja necessário seu deslocamento até a lavanderia. Para isso, será instalado um dispositivo **IoT-Home-L1**, capaz de detectar e informar, através de um site público, a intensidade luminosa do ambiente da lavanderia.

Leva-se em consideração a existência do sensor de presença já existente na lavanderia que acende a luz automaticamente na presença de alguém. Em um primeiro momento, a luz apagada por muito tempo deverá ser um indicador de lavanderia vazia. Assim, basta o condômino acompanhar de casa a utilização e descer assim que identificar uma pausa prolongada com a luz apagada.

Será isso suficiente para otimizar o uso da lavanderia do condomínio Recreio Canoas? Pode-se ainda, caso o projeto se mostre promissor, identificar individualmente os equipamentos ligados, de forma automática. Para isso, o dispositivo **IoT-Home-L1** deverá ser equipado com sensores nas respectivas tomadas de equipamentos. Mas essa seria uma segunda parte do projeto.


| **CONFLITO**     | **Nome**              | **Descrição**           |  
| :---             |     :---:             |          :---:          |  
| Objetivo         | **nome do objetivo**  |  descrição do objetivo  |
| Requisito 1      | **nome do requisito** |  descrição do requisito |  
| Pré 1            | **nome do requisito** |  descrição do requisito |   
| Requisito 2      | **nome do requisito** |  descrição do requisito | 

Uma breve análise das setas que interligam os elementos permite identificar possíveis pontos fracos no conflito:

| **ANÁLISE**      | **Nome**              | **Descrição**           |  
| :---             |     :---:             |          :---:          |  
| r1               | **nome do requisito** |  descrição do requisito |  
| p1               | **nome do requisito** |  descrição do requisito |  
| r2               | **nome do requisito** |  descrição do requisito |  
| p2               | **nome do requisito** |  descrição do requisito |  
| c                | **nome do requisito** |  descrição do requisito |      

