# Projeto End-to-End-  Análise de pedidos da Olist

Neste projeto, apliquei conceitos técnicos de Engenharia e Análise de Dados para criar um pipeline completo. **O objetivo foi aprimorar o pensamento analítico e responder a perguntas de negócio estratégicas, transformando dados brutos em um dashboard de tomada de decisão.**

![Tela 1](Dashboard\Imagens\Tela_1.png)

![Tela 2](Dashboard\Imagens\Tela_2.png)


### 1° Etapa do projeto- Ingestão e tratamento dos dados.

Nesta etapa, coloquei em prática o processo de ETL utilizando Python e Pandas:

- Extrai os dados de sete tabelas .csv  que obtive no site do Kaggle e que estavam armazenadas em uma pasta local.
- Realizei o tratamento dos dados separando cada função por tabela, onde pude tratar nulos, identificar duplicidade e removê-las, mudar o tipo dos dados, além de padronizar os textos de cada tabela.
- Na etapa final do pipeline, carreguei os dados tratados em um banco de dados relacional no PostgreSQL.

### 2° Etapa do projeto- Análise dos dados

Na Etapa final do projeto, estruturei o modelo Star Squema( fatos e dimensões) e analisei os dados no Power BI por meio da criação de medidas DAX:

- Taxa de atraso de pedidos
- Taxa de cancelamento
- Ticket medio dos produtos
- Receita total
- Custo de frete médio,
- Lead time médio,
- Formatação condicional
- Variação MoM
- Criação de tabela de calendário

A partir dessas medidas, pude analisar o comportamento dos pedidos, como o faturamento total e o ticket médio por categoria, taxa de cancelamento de cada categoria, avaliei se existia correlação entre a taxa de atraso dos pedidos e o cancelamento, além de verificar o lead time médio por cada categoria.

### Principais insights gerados:

* Durante os três anos, o estado de São Paulo permaneceu liderando na quantidade de vendas e isso ocorre porque cerca de 60% dos vendedores e 42% dos clientes estão concentrados nessa região, o que gera uma proporção de aproximadamente 23 clientes para cada vendedor.
* A categoria de Pc's tem produtos de alto valor, fretes mais elevados e tem uma taxa de cancelamento do pedido próxima de zero. A partir disso, cheguei à conclusão de que isso ocorre porque produtos caros e frágeis exigem seguros de carga mais altos das transportadoras, o que encarece o frete e os clientes não cancelam justamente pelo valor do item.
* Os produtos da categoria "Móveis e escritório" tem o lead time médio geral mais elevado, uma taxa de atraso dos pedidos em 8,05%, além de fretes mais altos para estados da região norte como Roraima e Tocantins. Isso pode evidenciar a falta de pontos de redistribuição em áreas dessa região.
