# Tipos e tarefas de Machine Learning

## Visão geral

**Machine Learning (ML)**, ou aprendizado de máquina, é uma área da inteligência artificial em que sistemas aprendem padrões a partir de dados para realizar previsões, classificações, agrupamentos ou recomendações.

O aprendizado pode acontecer de diferentes formas. As três principais são:

1. **Aprendizado supervisionado**;
2. **Aprendizado não supervisionado**;
3. **Aprendizado por reforço**.

---

## 1. Aprendizado supervisionado

No **aprendizado supervisionado**, o modelo aprende com exemplos que já possuem uma resposta conhecida. Esses exemplos podem estar em uma base de dados, textos, imagens, arquivos ou outros tipos de informação.

O modelo identifica a relação entre os dados de entrada e os resultados esperados para, posteriormente, fazer previsões sobre novos dados.

### Exemplo

Se fornecermos ao modelo diversos registros de imóveis contendo:

- área do apartamento;
- localização;
- quantidade de quartos;
- valor do aluguel;

ele poderá aprender a estimar o preço de um novo apartamento com características semelhantes.

> Em uma automação RPA, o sistema normalmente segue regras e etapas previamente definidas. Isso é diferente de um modelo de Machine Learning, que aprende padrões a partir de dados.

---

## 2. Aprendizado não supervisionado

No **aprendizado não supervisionado**, o modelo recebe dados sem respostas previamente identificadas. Seu objetivo é encontrar padrões, relações ou estruturas nos próprios dados.

O modelo pode, por exemplo, identificar grupos de pessoas com comportamentos semelhantes ou encontrar relações entre produtos consumidos por diferentes usuários.

> O aprendizado não supervisionado não significa simplesmente responder com base em probabilidade. Ele envolve a descoberta de padrões e estruturas sem rótulos fornecidos antecipadamente.

---

## 3. Aprendizado por reforço

No **aprendizado por reforço**, o sistema aprende por tentativa e erro. Ele realiza ações em um ambiente e recebe uma recompensa quando se aproxima do resultado esperado ou uma penalização quando toma uma decisão inadequada.

Com o tempo, o modelo busca aprender quais ações aumentam suas recompensas.

### Exemplo

Um sistema que aprende a jogar um jogo pode:

- receber uma recompensa quando vence uma partida;
- receber uma penalização quando perde;
- testar diferentes estratégias até encontrar as que produzem melhores resultados.

Esse tipo de aprendizado pode ser comparado a um processo de tentativa, avaliação e aperfeiçoamento contínuo.

---

## Principais tarefas de Machine Learning

As tarefas mais comuns de Machine Learning incluem:

| Tarefa | Objetivo | Exemplo |
|---|---|---|
| **Classificação** | Identificar uma categoria | Classificar um e-mail como spam ou não spam |
| **Regressão** | Prever um valor numérico | Estimar o preço de um aluguel |
| **Agrupamento ou clusterização** | Agrupar itens semelhantes | Separar clientes por perfil de consumo |
| **Recomendação** | Sugerir itens relevantes | Recomendar filmes ou produtos |

---

## Classificação

A **classificação** é utilizada quando o resultado esperado pertence a uma categoria.

### Exemplos

- Identificar se uma transação é fraudulenta ou legítima;
- Classificar uma imagem como contendo gato, cachorro ou outro animal;
- Determinar se um cliente tem alta, média ou baixa probabilidade de cancelar um serviço.

---

## Regressão

A **regressão** é utilizada para prever valores numéricos.

### Exemplo: previsão do aluguel de um apartamento

Podemos ensinar ao modelo os seguintes exemplos:

| Área do apartamento | Valor do aluguel |
|---:|---:|
| 50 m² | R$ 1.000,00 |
| 60 m² | R$ 1.200,00 |
| 70 m² | R$ 1.400,00 |

A partir desses dados, o modelo identifica uma relação entre a área do apartamento e o valor do aluguel. Se perguntarmos quanto poderia custar o aluguel de um apartamento com **55 m²**, o modelo poderá estimar um valor próximo de **R$ 1.100,00**, considerando apenas o padrão observado nos exemplos.

> Na prática, o preço também pode depender de localização, número de quartos, estado do imóvel, condomínio, vagas de garagem e outros fatores.

---

## Agrupamento ou clusterização

O **agrupamento**, também chamado de **clusterização**, organiza dados em grupos com características semelhantes, sem que esses grupos tenham sido definidos previamente.

### Exemplo: perfis de locatários

Ao analisar dados de comportamento, o modelo pode identificar grupos como:

- **Grupo 1:** pessoas com mais de 60 anos, aposentadas, que tendem a alugar apartamentos mais isolados no interior;
- **Grupo 2:** pessoas mais jovens, estudantes universitários, que tendem a procurar apartamentos próximos ao metrô.

Esses grupos não precisam ser informados previamente. Eles podem ser descobertos pelo próprio modelo a partir dos padrões encontrados nos dados.

> Os grupos representam tendências observadas nos dados. Eles não devem ser tratados como regras absolutas para todas as pessoas.

---

## Sistemas de recomendação

Os **sistemas de recomendação** sugerem itens com base em informações como:

- histórico de consumo;
- preferências do usuário;
- comportamento de usuários semelhantes;
- contexto da utilização;
- popularidade ou tendências recentes.

### Exemplo: recomendação de filmes

Se um usuário assistiu, nos últimos 30 dias, a:

- 5 filmes de ação;
- 1 filme de terror;
- 1 filme de romance;

a Netflix ou outro serviço de streaming poderá recomendar mais filmes de ação, pois esse gênero aparece com maior frequência no histórico recente do usuário.

Essa recomendação não é uma certeza sobre o que o usuário deseja assistir, mas uma previsão baseada nos padrões identificados.

---

## Pontos de atenção

### 1. Overfitting

**Overfitting**, ou **sobreajuste**, ocorre quando o modelo memoriza excessivamente os dados usados no treinamento, em vez de aprender padrões gerais.

Como consequência, o modelo pode apresentar um desempenho muito bom nos exemplos que já conhece, mas falhar quando recebe dados novos.

#### Exemplo

Imagine um modelo treinado para reconhecer gatos que memoriza detalhes específicos das imagens de treinamento, como o fundo ou a posição do animal. Quando recebe a imagem de um gato em outro ambiente, pode não conseguir identificá-lo corretamente.

#### Como reduzir o overfitting

Algumas estratégias incluem:

- utilizar mais dados de treinamento;
- separar os dados em treino, validação e teste;
- simplificar o modelo;
- aplicar técnicas de regularização;
- realizar validação cruzada;
- remover dados duplicados ou inadequados.

> O objetivo não é fazer o modelo decorar os exemplos, mas aprender padrões que possam ser aplicados a situações novas.

### 2. Drift do modelo

O **drift do modelo** acontece quando os dados ou os padrões do mundo real mudam ao longo do tempo. Como o modelo foi treinado com informações antigas, suas previsões podem perder qualidade.

#### Exemplo

Suponha que um modelo tenha sido treinado com dados que indicavam a existência de **500.000 apartamentos para alugar em São Paulo**. No dia seguinte, esse número pode mudar para **500.100**, além de haver alterações nos preços, na procura e nas regiões mais valorizadas.

Se o modelo não receber dados atualizados e não for monitorado, poderá começar a produzir previsões menos precisas.

#### Como lidar com o drift

É importante:

- monitorar continuamente o desempenho do modelo;
- atualizar a base de dados periodicamente;
- comparar previsões com resultados reais;
- identificar mudanças no comportamento dos dados;
- retreinar o modelo quando necessário.

---

## Conclusão

Machine Learning pode aprender de diferentes maneiras, dependendo do problema e dos dados disponíveis:

- o **aprendizado supervisionado** utiliza exemplos com respostas conhecidas;
- o **aprendizado não supervisionado** encontra padrões em dados sem rótulos;
- o **aprendizado por reforço** aprende por meio de ações, recompensas e penalizações.

Entre as principais tarefas estão **classificação, regressão, agrupamento e recomendação**. Para que um modelo continue confiável, é essencial evitar o **overfitting** e acompanhar possíveis mudanças nos dados, conhecidas como **drift do modelo**.
