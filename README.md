# Explorando a Curva de Phillips e a Lei de Okun: Modelagem VAR nos Países Nórdicos

Análise econométrica das relações entre inflação, desemprego e atividade econômica em Dinamarca, Suécia, Finlândia, Noruega e Islândia entre 2003 e 2023, utilizando modelos VAR, testes de causalidade de Granger, funções impulso-resposta e decomposição da variância.

## Contexto

A Curva de Phillips e a Lei de Okun figuram entre as relações macroeconômicas mais estudadas na literatura econômica. Este trabalho investiga a validade empírica dessas teorias nos países nórdicos, comparando a Dinamarca com Suécia, Finlândia, Noruega e Islândia por meio de técnicas de séries temporais.

O objetivo é analisar como choques na atividade econômica, desemprego e inflação se propagam ao longo do tempo e verificar se os padrões observados estão alinhados às previsões teóricas.

---

## Estrutura do Repositório

### 📄 TCC.pdf

Versão completa da monografia apresentada ao curso de Ciências Econômicas do IBMEC.

### 📊 Nordic_Phillips_and_Okun_VAR_Analysis.pdf

Slides utilizados para fins de síntese do projeto.

### 📂 graficos/

Conjunto de gráficos e diagnósticos gerados durante a modelagem econométrica.

**Séries Temporais**

* Evolução histórica das variáveis macroeconômicas.
* Séries em nível e componentes cíclicos obtidos pelo filtro HP.

**Raízes Inversas do Polinômio**

* Avaliação da condição de estabilidade dos modelos VAR.

**Funções Impulso-Resposta (FIR)**

* Resposta dinâmica das variáveis a choques ortogonalizados.

**Decomposição da Variância**

* Participação relativa de cada variável na explicação dos erros de previsão ao longo do horizonte temporal.

---

## Metodologia

### 1. Extração dos Ciclos Econômicos

Aplicação do filtro Hodrick-Prescott (HP), com λ = 1600, para obtenção dos hiatos do produto e desemprego.

### 2. Testes de Estacionariedade

Aplicação dos testes:

* Dickey-Fuller Aumentado (ADF)
* Phillips-Perron (PP)
* KPSS

para verificar a estacionariedade das séries e sua integração de ordem I(0).

### 3. Modelagem VAR

Foram estimados dois sistemas VAR:

**Modelo 1 — Curva de Phillips**

* Inflação
* Hiato do desemprego

**Modelo 2 — Lei de Okun**

* Hiato do produto
* Hiato do desemprego

A seleção de defasagens foi realizada pelo Critério de Informação de Schwarz (SIC), complementada pelos testes de causalidade de Granger.

### 4. Diagnóstico dos Modelos

Avaliação dos resíduos por meio dos testes:

* LM (autocorrelação serial)
* Jarque-Bera (normalidade)
* White (heterocedasticidade)

### 5. Tratamento de Quebras Estruturais

Utilização de indicadores de saturação (IIS e SIS) para capturar eventos extremos e minimizar vieses de estimação associados a choques exógenos relevantes, como:

* Crise Financeira Global de 2008
* Pandemia de Covid-19 em 2020

---

## Principais Resultados

### Lei de Okun

Foi observada evidência estatística consistente para Dinamarca, Finlândia e Suécia.

Um aumento de 1% no hiato do produto esteve associado a reduções entre 1,9% e 2,1% no hiato do desemprego.

### Curva de Phillips

Não foram encontradas evidências estatísticas robustas de um trade-off estrutural entre inflação e desemprego para o período analisado.

### Dinâmica dos Choques

A decomposição da variância indicou forte influência dos choques de produto sobre o desemprego, enquanto a inflação apresentou comportamento predominantemente exógeno nas economias avaliadas.

---

## Ferramentas Utilizadas

* EViews
* Python (visualização de dados)
* Microsoft Excel

---

## Autor

Rodrigo Emanuel Freitas Losada
