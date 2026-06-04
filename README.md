# Explorando a Curva de Phillips e a Lei de Okun: Modelagem VAR nos Países Nórdicos

Este repositório contém a monografia e os materiais complementares do trabalho de conclusão de curso em **Ciências Econômicas** pelo **IBMEC**. O estudo realiza uma análise econométrica aprofundada comparando a Dinamarca com os demais países nórdicos (Suécia, Finlândia, Noruega e Islândia) no período de 2003 a 2023.

### 📁 Estrutura do Repositório

* 📄 **`TCC.pdf`**: Documento completo da monografia.
* 📊 **`apresentaçao_slides.pdf`**: Deck de slides utilizado para a defesa e exposição do trabalho.
* 📂 **`gráficos/`**: Diretório contendo as exportações visuais e diagnósticos gerados na modelagem:
    * `Series_Temporais`: Comportamento histórico e estacionário das variáveis macroeconômicas.
    * `Raizes_Inversas_Polinomio`: Teste de estabilidade matemática atestando a robustez dos modelos VAR.
    * `FIR` (Funções Impulso-Resposta): Gráficos ilustrando a dinâmica e a resposta temporal dos hiatos a choques ortogonalizados.
    * `Decomposicao de Variância`: Análise de endogeneidade, mostrando o percentual da variância do erro de previsão explicado pelas próprias variáveis ao longo do tempo.

### 🔬 Metodologia e Pipeline de Dados

O projeto adota uma modelagem estatística rigorosa para o tratamento de séries temporais macroeconômicas:
* **Extração de Ciclos:** Utilização do Filtro Hodrick-Prescott (HP) com $\lambda = 1600$ para isolar o componente cíclico (hiato) do Produto, do Desemprego e da Inflação.
* **Estacionariedade:** Verificação das séries estacionárias de ordem $I(0)$ através dos testes de raiz unitária Dickey-Fuller Aumentado (ADF), Phillips-Perron (PP) e KPSS.
* **Vetor Autorregressivo (VAR):** Construção empírica de dois sistemas simultâneos, validados pelo teste de Causalidade de Granger e dimensionados pelo critério de informação de Schwarz (SIC):
    * *Modelo 1:* Focado na Curva de Phillips (Inflação vs. Hiato do Desemprego).
    * *Modelo 2:* Focado na Lei de Okun (Hiato do Desemprego vs. Hiato do PIB).
* **Diagnóstico de Resíduos:** Avaliação de adequação através dos testes LM (ausência de autocorrelação serial), Jarque-Bera (normalidade) e White (homoscedasticidade).
* **Tratamento de Quebras Estruturais:** Inserção de variáveis *dummy* via indicadores de saturação (IIS e SIS) para absorver o impacto de choques atípicos extremos, como a Crise Financeira Global (2008) e a Pandemia da Covid-19 (2020), mitigando vieses de estimação.

### 📈 Principais Resultados

1.  **Lei de Okun Validada:** Constatou-se significância estatística robusta na Dinamarca, Finlândia e Suécia. Um aumento de 1% no hiato do PIB demonstrou reduzir o hiato do desemprego entre -1.9% e -2.1%.
2.  **Curva de Phillips Não Validada:** Os coeficientes não apresentaram significância estatística simultânea, indicando ausência de um *trade-off* estrutural claro entre inflação e desemprego para a amostra e período avaliados.
3.  **Dinâmica de Choques:** A Decomposição da Variância revelou uma forte endogeneidade do hiato do desemprego (fortemente responsivo aos choques de produto), contrastando com a natureza primariamente exógena da inflação nas economias avaliadas.

### 👨‍💻 Autor

**Rodrigo Emanuel Freitas Losada**
