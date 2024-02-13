# Painel de Nível de Instrução Básica no Brasil 

## Contexto
O IBGE (Instituto Brasileiro de Geografia e Estatística) é um dos maiores provedores de informação no território nacional. 
Além da disponibilização de um recurso de API para consumo de dados abertos, também é possível encontrar outros dados resultados de pesquisas e análises estatísticas
conduzidas pelo Instituto. 

Para este projeto, foram utilizados dados de 2012-2016 sobre alfabetização e outros graus de instrução como ensino fundamental e médio e será conduzida uma análise sobre diversidade. 

## Informações 

Neste projeto, foram utilizados as seguintes ferramentas:

<li> Excel:https://www.microsoft.com/pt-br/microsoft-365/excel </li>
<li> Power BI: https://powerbi.microsoft.com/ </li>
<li> Portal do IBGE : https://www.ibge.gov.br/acesso-informacao/estatisticas.html </li>

Os dados estão disponíveis e tratados neste mesmo repositório, salvos no arquivo em csv. 

## Objetivo

Os dois principais objetivos deste projeto são: construir um painel gerencial e realizar análises, gerar informação a partir dos dados disponíveis.

# Análise sobre Nível de Instrução Básica no Brasil 

## 1) Tratamento de dados + Importação no Power BI

Os dados estavam disponíveis em planilha no site do IBGE, foram convertidas as linhas em colunas e padronizadas os nomes das colunas para facilitar o consumo 
das informações. Em seguida, o arquivo foi salvo em csv e importado no Power BI. 

## 2) Relacionamentos no Power BI 

Foi aplicado o modelo de Star-Schema, o qual foi construído a partir de 2 tabelas fato, ou seja, 2 tabelas de eventos e 3 tabelas dimensões a partir das dimensões 
de Raça/Cor, Sexo e Tempo, que são analisadas simultaneamente em ambas as tabelas fato. O modelo está evidenciado na imagem abaixo:

<img width="450" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/843607a3-34ce-435a-8eca-97c2c23bfd7d">
