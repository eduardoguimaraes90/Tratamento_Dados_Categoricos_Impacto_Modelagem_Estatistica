# Tratamento de Dados Categóricos e o Impacto em Modelagem Estatística

**Projeto 5 do curso Matemática e Estatística Aplicada Para Data Science, Machine Learning e IA da Data Science Academy**

O Projeto 5 foca no tratamento de dados categóricos e seu impacto na modelagem estatística, destacando a importância de abordagens adequadas para a manipulação de variáveis não numéricas em análises preditivas. Dados categóricos, que representam categorias ou grupos, como gênero, nacionalidade ou status de cliente, apresentam desafios únicos em termos de modelagem estatística, uma vez que muitos algoritmos de Machine Learning e técnicas estatísticas requerem entrada numérica.

## Objetivo

Este projeto visa explorar e aplicar diferentes técnicas de codificação e transformação de variáveis categóricas, como:
- **One-Hot Encoding**
- **Ordinal Label Encoding**

O objetivo é preparar os dados para análise, investigando o impacto dessas técnicas na performance de modelos estatísticos.

## Conceitos

### One-Hot Encoding
O **One-Hot Encoding** é uma técnica que transforma variáveis categóricas em um formato compreensível para algoritmos de Machine Learning. Para cada categoria de uma variável, cria-se uma nova coluna binária que assume o valor 1 quando a categoria está presente e 0 caso contrário. Por exemplo:

| Categoria | A | B | C |
|-----------|---|---|---|
| A         | 1 | 0 | 0 |
| B         | 0 | 1 | 0 |
| C         | 0 | 0 | 1 |

Essa abordagem evita que os algoritmos interpretem valores categóricos como quantitativos, o que poderia levar a resultados incorretos.

### Ordinal Label Encoding
O **Ordinal Label Encoding** é uma técnica que converte categorias em valores numéricos com base em uma ordem hierárquica. Cada categoria é representada por um inteiro que reflete sua posição relativa. Por exemplo, para os tamanhos de roupas (Pequeno, Médio, Grande):

| Categoria | Valor |
|-----------|-------|
| Pequeno   | 1     |
| Médio     | 2     |
| Grande    | 3     |

Essa abordagem é útil quando há uma relação ordinal entre as categorias, mas deve ser usada com cuidado para evitar a introdução de suposições erradas nos modelos.

### Modelagem Preditiva
A **modelagem preditiva** é o processo de usar dados históricos para prever resultados futuros. Isso é feito construindo modelos estatísticos ou de aprendizado de máquina que aprendem padrões nos dados e os aplicam a novos conjuntos de dados. Em aplicações práticas, a modelagem preditiva pode ser usada em diversas áreas, como previsão de vendas, análise de riscos e manutenção preditiva.

#### Etapas Comuns da Modelagem Preditiva:
1. **Coleta de Dados**: Obtenção de dados históricos relevantes.
2. **Pré-Processamento**: Limpeza e transformação dos dados para eliminar inconsistências.
3. **Divisão de Dados**: Separação dos dados em conjuntos de treinamento e teste.
4. **Construção do Modelo**: Treinamento de algoritmos para aprender padrões nos dados.
5. **Validação**: Avaliação da precisão e generalização do modelo.

### Modelagem Estatística
A **modelagem estatística** é um método de análise que utiliza técnicas matemáticas para descrever, explicar e prever relações entre variáveis. Diferente da modelagem preditiva, que pode usar métodos baseados em aprendizado de máquina, a modelagem estatística frequentemente se concentra em entender os dados e derivar insights baseados em relações matemáticas.

#### Exemplos de Modelos Estatísticos:
- **Regressão Linear**: Avalia a relação linear entre uma variável dependente e uma ou mais independentes.
- **Análise de Variância (ANOVA)**: Compara médias entre grupos para identificar diferenças significativas.
- **Modelos de Probabilidade**: Usados para prever a probabilidade de eventos futuros com base em dados históricos.

## Etapas do Projeto

1. **Modelagem Preditiva**:
   - **Problema**: Prever o custo de entrega através de um modelo.
   - **Conclusão**: O coeficiente de determinação (R²) do modelo apresentou aproximadamente 42%, indicando que o modelo explicou cerca de 42% da variabilidade da variável alvo. Esse resultado demonstra a importância de melhorar a seleção de variáveis e técnicas de codificação para aumentar a capacidade preditiva do modelo.
     
   ![image](https://github.com/user-attachments/assets/fbb9a9ed-8de4-4a26-a9e2-211310bca3dc)

2. **Modelagem Estatística**:
   - **Problema 2**: Identificar a relação entre o custo de entrega e as outras variáveis.
   - **Conclusão**:
     - A interpretação dos coeficientes no modelo de regressão linear revelou insights importantes sobre a influência de cada variável preditora no custo de entrega.

## Resultados

### Interpretação dos Coeficientes
A interpretação dos coeficientes em um modelo de regressão linear fornece insights sobre como cada variável preditora (ou "feature") influencia a variável alvo, assumindo que todas as outras variáveis no modelo permaneçam constantes.

![Visualização dos Resultados](https://github.com/user-attachments/assets/8b052aea-e784-405e-85e3-9f732797c3a7)

#### Exemplos de Coeficientes
- **cliente_local_Sim (9.048919)**: Quando o cliente é local (*Sim*), espera-se, em média, um aumento de aproximadamente 9.05 unidades no custo de entrega, comparado a quando o cliente não é local (base ou referência), mantendo as demais variáveis constantes. Esta variável tem o impacto mais significativo entre as examinadas.

#### Interpretação Geral
- Variáveis com coeficientes **positivos** aumentam o custo de entrega quando aumentam (ou estão presentes, no caso de variáveis categóricas binárias como *cliente_local_Sim*).
- Variáveis com coeficientes **negativos** diminuem o custo de entrega quando aumentam.
- A **magnitude** do coeficiente indica o tamanho do efeito: variáveis com coeficientes maiores têm um impacto mais significativo na variável alvo.

## Considerações Finais

Os efeitos modelados assumem que todas as outras variáveis permanecem constantes, o que nem sempre reflete a realidade prática. É essencial realizar análises adicionais para validar esses resultados em cenários reais.
