# Lighthouse
Respondendo as questões da Lighthouse


1.	Faça uma análise exploratória dos dados (EDA), demonstrando as principais características entre as variáveis e apresentando algumas hipóteses de negócio relacionadas. Seja criativo!


2.	Responda também às seguintes perguntas:
a.	Supondo que uma pessoa esteja pensando em investir em um apartamento para alugar na plataforma, onde seria mais indicada a compra?

Utilizando o conceito de agrupamento, cheguei em duas possibilidades:

RECOMENDAÇÃO PARA INVESTIMENTO 1:
Bairros com maior potencial de investimento:
                     price       numero_de_reviews
                      mean count              mean
bairro                                            
Fort Wadsworth  800.000000     1          0.000000
Woodrow         700.000000     1          0.000000
Tribeca         490.638418   177         11.491525
Sea Gate        487.857143     7          1.428571
Riverdale       442.090909    11         26.636364

RECOMENDAÇÃO PARA INVESTIMENTO 2:
Grupo de bairros com maior potencial de investimento:
                    price        numero_de_reviews
                     mean  count              mean
bairro_group                                      
Manhattan      196.875814  21661         20.985596
Brooklyn       124.381983  20103         24.203601
Staten Island  114.812332    373         30.941019
Queens          99.517649   5666         27.700318
Bronx           87.496792   1091         26.004583

Consideraria na recomendação 1, não utilizar o bairro Fort Wadsworth ou Woodrow, pois ambos tem apenas 1 imóvel, podendo tornar a contagem unilateral.

b.	O número mínimo de noites e a disponibilidade ao longo do ano interferem no preço?

Quando olhamos através de regressão linear e média, não é possivel identificar alguma relação no preço quando aplicamos os dois parametros, porém, quando avaliamos pelos maiores valores, conseguimos identificar que os maiores alugueis como pratica usam poucos dias como minimo de noites, provavelmente pelo elevado preço.

c.	Existe algum padrão no texto do nome do local para lugares de mais alto valor?

Eles mostram a localização e vista no nome, para evidenciar os diferenciais deles.

4.	Explique como você faria a previsão do preço a partir dos dados. Quais variáveis e/ou suas transformações você utilizou e por quê? Qual tipo de problema estamos resolvendo (regressão, classificação)? Qual modelo melhor se aproxima dos dados e quais seus prós e contras? Qual medida de performance do modelo foi escolhida e por quê?

A previsão de preço seria de uma média de 302 Dolares, fiz uma analise filtrando o bairro e filtrando pelo room_type e tirei uma média. Estamos resolvendo por regressão, uma vez que queremos encontrar um valor.

Fiz um modelo analisando as intermediações, você acaba analisando bem quanto vale em média apartamentos a sua volta, porém existiriam outras analises que deveriam ser feitas, como metragem, localização com base em rua, acessos e afins dentro do bairro e analise de interior, portanto a chance do valor estar longe do real, pode ser bem grande.

5.	Supondo um apartamento com as seguintes características:

{'id': 2595,
 'nome': 'Skylit Midtown Castle',
 'host_id': 2845,
 'host_name': 'Jennifer',
 'bairro_group': 'Manhattan',
 'bairro': 'Midtown',
 'latitude': 40.75362,
 'longitude': -73.98377,
 'room_type': 'Entire home/apt',
 'minimo_noites': 1,
 'numero_de_reviews': 45,
 'ultima_review': '2019-05-21',
 'reviews_por_mes': 0.38,
 'calculado_host_listings_count': 2,
 'disponibilidade_365': 355}

Qual seria a sua sugestão de preço?

A previsão de preço seria de uma média de 302 Dolares, fiz uma analise filtrando o bairro e filtrando pelo room_type e tirei uma média.

5.	Salve o modelo desenvolvido no formato .pkl. 
6.	A entrega deve ser feita através de um repositório de código público que contenha:
a.	README explicando como instalar e executar o projeto
b.	Arquivo de requisitos com todos os pacotes utilizados e suas versões
c.	Relatórios das análises estatísticas e EDA em PDF, Jupyter Notebook ou semelhante conforme passo 1 e 2.
d.	Códigos de modelagem utilizados no passo 3 (pode ser entregue no mesmo Jupyter Notebook).
e.	Arquivo .pkl conforme passo 5 acima.
7.	Um vídeo curto explicando o desenvolvimento de suas entregas deste desafio, como você planejou e executou as atividades propostas. O vídeo deverá ser entregue via link via Google Drive. Lembre-se de autorizar o acesso para "qualquer pessoa com o link".
