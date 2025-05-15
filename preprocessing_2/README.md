## ⚙️ Etapa de Pré Processamento (Parte II) 
Nessa etapa, foi realizado análises univariadas e bivariadas a fim de entender as variáveis mais a fundo e a relação delas com a classe (Churn). 

### Análise Univariada
- **Estatísticas Básicas**: Nessa análise, podemos ver que a variável **Total_Pago** é a que possui maior variação de dados, pois a sua média era muito discrepante do valor máximo, porém ainda estava dentro do esperado e, por isso, não senti necessidade de fazer algum tratamento. 
- **Variáveis Categóricas**: 
    - Gênero: Existe um equilíbrio grande; 
    - Método de Pagamento: A classe que se sobressai é a de Cheque Eletrônico;
    - Churn (Classe): Existem muito mais clientes Não Churn do que Churn;
    - Tipo de Contrato: O contrato que maior se sobressai entre os clientes é o Mês a Mês;
    - Streaming de TV: Existe um certo equilíbrio entre clientes que solicitaram ou não um serviço de Streaming para TV, enquanto existe uma baixa grande em clientes que não possuem serviço de internet. <br>
[![Gráfico](https://img.shields.io/badge/Gênero-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/genero.png)
[![Gráfico](https://img.shields.io/badge/Método_de_Pagamento-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/metodo_pagamento.png)
[![Gráfico](https://img.shields.io/badge/Churn-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/churn.png)
[![Gráfico](https://img.shields.io/badge/Tipo_de_Contrato-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/tipo_contrato.png)
[![Gráfico](https://img.shields.io/badge/Streaming_TV-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/streamingtv.png)
- **Variáveis Booleanas**: 
    - Casado: Possui bastante equilíbrio nessa variável;
    - Dependentes: Existem muito mais clientes que não possuem dependentes; 
    - Idoso: Existem muito mais clientes que não são idosos; <br>
[![Gráfico](https://img.shields.io/badge/Casado-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/casado.png)
[![Gráfico](https://img.shields.io/badge/Dependentes-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/dependentes.png)
[![Gráfico](https://img.shields.io/badge/Idoso-skyblue?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/idoso.png)
### Análise Bivariada
- **Relação entre Gênero e Churn**: Essa relação é bem fraca, onde podemos notar que existe um equilíbrio bem grande entre os gêneros que são ou não Churn; 
- **Relação entre Idoso e Churn**: É notável que quando o cliente é Churn, existe uma porcentagem deles que são idosos também, mas é uma porcentagem sutil; 
- **Relação entre Tempo como Cliente e Churn**: Essas variáveis possuem uma relação muito forte, onde podemos notar que quanto menor o tempo como cliente, mais propenso ele é de ser Churn;
- **Relação entre Tipo de Contrato, Total Pago e Churn**: Pode-se notar que, para clientes Churn, a partir do tipo de contrato de 1 ano, os clientes possuem um total pago maior e a quantidade de clientes diminui também.
- **Relação entre Método de Pagamento e Churn**: O método de pagamento mais utilizado quando se é Churn é o Cheque Eletrônico;
- **Relação entre Casado e Churn**: É notável que maioria dos clientes Churn não são casados, enquanto que mais da metade dos clientes que não são Churn, são casados;
- **Relação entre Servico de Internet e Churn**: O Serviço de Internet mais utilizado por clientes Churn é o de Fibra Otica. <br>
  [![Gráfico](https://img.shields.io/badge/Gênero_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/genero_churn.png)
  [![Gráfico](https://img.shields.io/badge/Idoso_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/idoso_churn.png)
  [![Gráfico](https://img.shields.io/badge/Tempo_Cliente_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/tempo_cliente_churn.png)
  [![Gráfico](https://img.shields.io/badge/Contrato_Total_Pago_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/total_pago_contrato_churn.png)
  [![Gráfico](https://img.shields.io/badge/Método_Pagamento_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/metodo_pagamento_churn.png)
  [![Gráfico](https://img.shields.io/badge/Casado_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/casado_churn.png)
  [![Gráfico](https://img.shields.io/badge/Serviço_Internet_Churn-darkgreen?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/churn-telecomunicacoes/blob/main/graficos/servi%C3%A7o_internet_churn.png)

### Variáveis com Maior Impacto sobre a Classe (Churn)
- De acordo com as análises realizadas anteriormente, as classes que possuem maior impacto sobre o cliente ser ou não Churn é, principalmente, o **Tempo_como_Cliente**, **Tipo_Contrato** e **Total_Pago**, pois é notável que o tempo como cliente influencia muito se ele vai se tornar Churn, principalmente nos primeiros meses como cliente, e por causa disso, o tipo de contrato de Mês a Mês precisa conter algum elemento que estimule o cliente a continuar, trazendo formas de desconto para que o seu total pago não seja tão elevado. 
- Outra variável que possui uma quantidade muito grande de clientes Churn é os que utilizaram Fibra Ótica no seu Serviço de Internet. É importante investigar se esse elemento está afetando o motivo do cliente se tornar Churn ou não. Isso também é notado em clientes que utilizaram o Cheque Eletrônico como Método de Pagamento, é uma quantidade muito discrepante entre os clientes que são Churn e, por isso, é importante verificar esse elemento.
