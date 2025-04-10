# 📞 Churn Telecomunicações
> **Autoria**: Millena Thalyne <br>
> **Curso**: Profissão Cientista de Dados - EBAC <br>
> **Linguagem**: Python <br>
> **Base de Dados**: Churn Telecon (serviços de internet, telefone e tv - Telecomunicação)

## Objetivo
Esse projeto é parte da formação Profissão Cientista de Dados da EBAC, onde faço todas as etapas da modelagem dos dados de Churn no contexto de serviços de internet, telefone e tv.
## Base de Dados
*   **CustomerID** : Esse é o ID único de cada cliente nosso da rede de produtos de telecomunicação.

*   **Genero** : O genero dos nossos clientes.

*   **Idoso** : Se nosso cliente tem acima de 60 anos ou não. (Sim = 1 | Não = 0)

*   **Casado** : Se nosso cliente é casado ou não.

*   **Dependents** : Se cliente tem dependentes.

*   **Tempo_como_Cliente** : Tempo em meses que nosso cliente está com a nossa empresa.

*   **PhoneService** : Se ele contratou serviço telefônico com a nossa empresa.

*   **Servico_Internet** : Qual o tipo de serviço de internet contratado.

*   **Servico_Seguranca** : Se ele contratou serviço de segurança com a nossa empresa.

*   **Suporte_Tecnico** : Se já acionou o suporte técnico.

*   **StreamingTV** : Se ele contratou serviço de streaming para TV.

*   **Tipo_Contrato** : Qual o tipo de contrato dos nossos clientes, se era mensal, anual etc.

*   **PaymentMethod** : Forma de Pagamento.

*   **Pagamento_Mensal** : Quanto o cliente pagava mensalmente.

*   **Total_Pago** : Total já pago pelo cliente para nossa companhia.

*   **Churn** : Nossa coluna mais importante, se nosso cliente nos abandonou ou não.
  
## Etapa de Pré Processamento
### Tipos de Dados
Assim que os dados foram lidos, foi verificado se os tipos de dados de cada uma das variáveis eram condizentes com os dados e sim, a princípio, os dados estão de acordo e não precisei fazer conversões. 
### Dados Faltantes
Após quantificar em porcentagem quais colunas estão com valores ausentes, foi possível analisar quais melhores métodos de tratamento, sendo eles: 
* **Tratamento de Nulo para a Coluna 'Gênero' e 'Churn'**: As colunas de Gênero e Churn são as com menores perdas (sendo 0.48% e 0.20%), e também é verificado que as linhas onde Churn é nulo, também contém Gênero nulo. Dessa forma, excluindo somente as linhas onde Gênero é nulo seria a maneira ideal para lidar com esse cenário, uma vez que a quantidade de dados faltantes não é tão grande e faria o tratamento nas duas colunas ao mesmo tempo;
* **Tratamento de Nulo para a Coluna 'Pagamento_Mensal'**: A coluna de Pagamento_Mensal contém 13% de dados ausentes e, por ser uma informação importante e do formato numérico, excluir esses registros seria uma perda muito maior do que o cenário anterior. Dessa forma, uma maneira ideal para lidar com esse caso é substituir os valores faltantes por uma medida estatística simples (seja ela a média, mediana ou, até mesmo, a moda). <br> Foi verificado qual medida estatística se enquadra mais nesse tratamento a partir das seguintes informações: A média e a mediana possuem uma diferença pequena, os dados estão bem distribuídos e a porcentagem de nulos não é acima de 15% (o que seria crítico), portanto utilizar a *média* para a coluna Pagamento_Mensal para tratamento de dados nulos é a maneira mais ideal. <br> *OBS: Você pode verificar o gráfico boxplot no [notebook de pré-processamento](URL)*;
* **Tratamento de Nulos para a Coluna 'PhoneService'**: A coluna de PhoneService, que é do tipo booleano (Sim ou Não), tem a maior porcentagem de dados faltantes (60%). <br> Como essa coluna possui uma porcentagem muito grande de dados nulos, se eu substituir por um dos lados (sim ou não) vai levar a um vies muito maior para um desses lados, o que eu não tenho certeza. Dessa forma, a maneira que irá preservar essa quantidade de dados e evitar o viés, sendo mais possível de interpretar, é adicionar uma terceira opção: Indefinido. 
### Padronização de Dados
Nessa etapa, foi verificado valores digitados incorretamente; letras maiúsculas ou minúsculas; dados iguais, porém escritos de forma diferente; dentre outros. Com isso, a única coluna que precisará de padronização nos dados:  
* Genero: Precisará de padronização para Female F ou f, e Male para M ou m.
### Renomear Nomes de Colunas
Para finalizar essa etapa, foi substituido os nomes das colunas pela tradução direta daqueles que estavam com eles em inglês: 
* 'customerID': 'ID';
* 'Dependents': 'Dependentes';
* 'PhoneService': 'Servico_Telefonico';
* 'StreamingTV': 'Streaming_TV';
* 'PaymentMethod': 'Metodo_Pagamento'.
