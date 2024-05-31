# Relatório de Análise de Dados e Predição de Preços de Aluguéis em São Paulo

## Introdução

Neste projeto, foi realizado uma análise detalhada dos preços de aluguéis na cidade de São Paulo utilizando técnicas de análise de dados e regressão linear com a biblioteca Pandas e o pacote `statsmodels` em Python. O objetivo principal foi explorar e modelar a relação entre as variáveis do conjunto de dados e os preços dos aluguéis, utilizando uma transformação logarítmica para lidar com a heterocedasticidade e outliers nos dados. A seguir, apresentamos as etapas realizadas, os resultados obtidos e as conclusões derivadas da análise.

## Etapas do Projeto

1. **Importação e Limpeza dos Dados**: 
   - Os dados foram importados e carregados em um DataFrame do Pandas. A limpeza incluiu a remoção de valores ausentes e a aplicação de transformações necessárias.
  
2. **Análise Descritiva**:
   - Realizamos uma análise descritiva das variáveis, incluindo estatísticas básicas como média, mediana, desvio padrão, e quartis.
   
3. **Transformação dos Dados**:
   - Foi aplicada a transformação logarítmica na variável dependente (`rent`) e na variável `area` para lidar com a heterocedasticidade e normalizar a distribuição dos dados.

4. **Modelagem de Regressão Linear**:
   - Ajustamos um modelo de regressão linear utilizando a transformação logarítmica das variáveis. Utilizamos a biblioteca `statsmodels` para ajustar o modelo e obter um resumo detalhado dos coeficientes e estatísticas.

5. **Avaliação do Modelo**:
   - Avaliamos o desempenho do modelo utilizando métricas como Mean Squared Error (MSE) e R-squared (R²). Também realizamos uma análise de resíduos para verificar a normalidade e a presença de padrões nos resíduos.

6. **Visualização dos Resultados**:
   - Criamos diversas visualizações para explorar a relação entre as variáveis e os clusters formados utilizando o algoritmo K-means.

## Resultados

### Análise Descritiva

A análise descritiva revelou que a média dos preços de aluguéis em São Paulo é significativamente influenciada por variáveis como a área do imóvel, o número de quartos e vagas na garagem. Observamos uma variação considerável nos preços, o que justifica a aplicação de técnicas avançadas para modelar a relação entre essas variáveis e os preços de aluguel.

### Modelagem de Regressão Linear

Utilizamos a transformação logarítmica para ajustar o modelo de regressão linear, resultando em um R² de 0.962, indicando que 96.2% da variação nos preços de aluguéis logarítmicos é explicada pelo modelo. Este é um ajuste excepcional, sugerindo que o modelo captura bem a variabilidade nos dados.

### Coeficientes do Modelo

- **Constante (const)**: 0.3239 (altamente significativo)
- **Logaritmo da Área Total (total_log)**: 0.9296 (altamente significativo)
- **Área (area)**: 0.0008 (altamente significativo)
- **Número de Quartos (bedrooms)**: -0.0092 (altamente significativo)
- **Número de Vagas na Garagem (garage)**: -0.0126 (altamente significativo)
- **Cluster**: -0.0114 (altamente significativo)

Os coeficientes sugerem que a área total do imóvel (em logaritmo) tem uma relação positiva forte com os preços de aluguel, enquanto o número de quartos e vagas na garagem apresentam uma relação inversa, embora significativas, o que pode ser um indicativo de peculiaridades específicas do mercado imobiliário de São Paulo.

### Avaliação dos Resíduos

A análise dos resíduos mostrou que os resíduos não seguem uma distribuição normal, conforme indicado pelos testes Omnibus e Jarque-Bera. No entanto, a estatística de Durbin-Watson sugere que não há autocorrelação significativa dos resíduos, o que é positivo para a validade do modelo.

## Conclusões e Recomendações

1. **Qualidade do Ajuste**:
   - O modelo logarítmico apresentou um excelente ajuste aos dados, explicando 96.2% da variação nos preços de aluguel. Este alto valor de R² indica que o modelo é robusto e confiável para previsões de preços de aluguel em São Paulo.

2. **Transformação Logarítmica**:
   - A transformação logarítmica foi eficaz em lidar com a heterocedasticidade e os outliers, resultando em um modelo mais estável e previsões mais precisas.

3. **Significância das Variáveis**:
   - Todas as variáveis independentes no modelo são altamente significativas, com exceção da constante, sugerindo que cada variável tem um impacto estatisticamente significativo nos preços de aluguel.

4. **Interpretação dos Coeficientes**:
   - A área total (em logaritmo) tem a maior influência positiva nos preços de aluguel, seguido pela área linear. A relação inversa do número de quartos e vagas na garagem com os preços de aluguel pode indicar particularidades do mercado imobiliário que merecem uma análise mais aprofundada.

5. **Multicolinearidade**:
   - A análise de VIF não indicou problemas significativos de multicolinearidade, com todos os valores de VIF abaixo de 10.

### Recomendações Finais

Para futuros estudos e modelos preditivos de preços de aluguel:

1. **Explorar Modelos Alternativos**:
   - Considerar explorar modelos de regressão robusta e técnicas de machine learning para comparar a performance e robustez das previsões.

2. **Analisar Outliers**:
   - Realizar uma análise detalhada dos outliers para entender melhor as peculiaridades do mercado e possivelmente ajustar o modelo para acomodar esses dados.

3. **Incluir Variáveis Adicionais**:
   - Incluir variáveis adicionais que possam influenciar os preços de aluguel, como localização geográfica, proximidade a serviços e infraestrutura urbana.

4. **Atualização Contínua do Modelo**:
   - Manter o modelo atualizado com dados mais recentes para garantir a precisão e relevância das previsões ao longo do tempo.


Este relatório fornece uma visão abrangente e detalhada da análise de dados e modelagem preditiva de preços de aluguel em São Paulo. Esperamos que os insights obtidos possam auxiliar na tomada de decisões estratégicas e no desenvolvimento de políticas de precificação mais eficazes.

## Anexos
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/1a1cb9e6-61b4-47c8-be45-586c91fd572f)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/556b1409-c780-4436-96b8-0c6c19572445)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/31be1cb0-5dd2-4440-abf3-719c1a7f2f21)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/c5657a6b-cf8a-4b3c-89f7-656dd756fe7c)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/f88dd953-73db-40ba-88bd-5d09567e4c22)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/b84a6bcc-1611-43be-b318-c698251dd01f)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/b8fca8a5-c52c-48dd-881c-a9bc2b624f59)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/409d3491-383e-4c24-935e-09d27fb6a02a)
<br>
![image](https://github.com/fzta492/analise_alugueis_sao_paulo/assets/76072907/0dde4c00-0c5d-4506-8a1c-2ac5577730f1)





