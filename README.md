# Dashboard de Performance de Campanhas de Marketing

## Sobre o projeto
Dashboard interativo em Power BI para análise de performance de campanhas 
de marketing digital, construído a partir de um dataset sintético de 200 mil 
campanhas (Kaggle).

## Ferramentas
Power BI Desktop (Power Query, DAX, modelagem de dados)

## Processo (ETL)
- Importação via Power Query
- Tratamento de tipos incorretos (conversão monetária com erro de localidade)
- Correção de campos percentuais mal escalados (Conversion_Rate, ROI)
- Remoção de coluna redundante, verificação de duplicatas e nulos
- Modelagem com tabela calendário (relacionamento 1-para-muitos)

## KPIs calculados (DAX)
- CTR (Taxa de Cliques)
- CPA (Custo por Aquisição)
- ROAS (Retorno sobre Investimento em Anúncios)
- Gasto Total e Receita Estimada

## Principais aprendizados / decisões técnicas
- Diferença entre coluna calculada e medida DAX (uso de SUMX para cálculos 
  linha a linha antes de agregar)
- Identificação e correção de dois bugs silenciosos de dado (formatação 
  regional e escala percentual) através de checagem cruzada com cálculo manual
- Uso de DIVIDE() para evitar erros de divisão por zero

## Observações sobre os dados
Por ser um dataset sintético, os valores não refletem benchmarks reais de 
mercado (ex: CTR de ~10%, bem acima da média real de 1-3%) e não apresentam 
variação significativa entre canais/empresas nem sazonalidade. A metodologia 
aplicada, no entanto, é a mesma usada em cenários de dados reais.

## Screenshots
