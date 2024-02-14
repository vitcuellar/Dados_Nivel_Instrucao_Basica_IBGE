# Painel de Nível de Instrução Básica no Brasil 

## Contexto
  O IBGE (Instituto Brasileiro de Geografia e Estatística) é um dos maiores provedores de informação no território nacional. 
Além da disponibilização de um recurso de API para consumo de dados abertos, também é possível encontrar outros dados resultados de pesquisas e análises estatísticas
conduzidas pelo Instituto. 
<br>
  Para este projeto, foram utilizados dados de 2012-2016 sobre alfabetização e outros graus de instrução como ensino fundamental e médio e será conduzida uma análise sobre diversidade. 

## 💻 Informações 

  Neste projeto, foram utilizados as seguintes ferramentas:
<br>
<li> Excel:https://www.microsoft.com/pt-br/microsoft-365/excel </li>
<li> Power BI: https://powerbi.microsoft.com/ </li>
<li> Portal do IBGE : https://www.ibge.gov.br/acesso-informacao/estatisticas.html </li>
<br>

**[Fontes de Dados]** Os dados estão disponíveis e tratados neste mesmo repositório, salvos no arquivo em csv. 

## Objetivos

  Os dois principais objetivos deste projeto são: construir um painel gerencial e realizar análises, gerar informação a partir dos dados disponíveis.

# Construção do Painel de Nível de Instrução 

## 1) Tratamento de dados + Importação no Power BI

  Os dados estavam disponíveis em planilha no site do IBGE, foram convertidas as linhas em colunas e padronizadas os nomes das colunas para facilitar o consumo 
das informações. Em seguida, o arquivo foi salvo em csv e importado no Power BI. 

## 2) Relacionamentos no Power BI 

  Foi aplicado o modelo de Star-Schema, o qual foi construído a partir de 2 tabelas fato, ou seja, 2 tabelas de eventos e 3 tabelas dimensões a partir das dimensões 
de Raça/Cor, Sexo e Tempo, que são analisadas simultaneamente em ambas as tabelas fato. O modelo está evidenciado na imagem abaixo:
<br>
<br>
<img width="500" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/843607a3-34ce-435a-8eca-97c2c23bfd7d">

## 3) Tabela de Medidas 

  Como foi decidido priorizar análises de média das taxas de alfabetização e proporção, criou-se uma tabela apenas de medidas que foram utilizadas de forma 
planejada no painel. As medidas também foram segmentadas para garantir que houvesse a interseccção entre as diversidades analisadas, leia-se como : mulheres brancas, mulheres pretas ou pardas, homens brancos e homens pretos ou pardos. Tal como disposto no início do painel, conforme imagem abaixo:
<br>
<br>
<img width="500" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/73e74bd8-0b6a-4558-98c8-3bd94da9dc59">


## 4) Filtros 

  Para as análises realizadas, foi definido como principais filtros exatamente as dimensões simultâneas às 2 tabelas fato. Sendo assim:
<br>
<br>
<img width="150" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/312cceb6-319e-4842-bfc9-d3a97b9513ca">

## 5) Resumo Inteligente 

  Também foi aplicado o recurso de Narrativa Inteligente do Power BI, para resumir de forma assertiva as principais informações das principais visões do Painel. Sendo assim, foi definido como importante a comparação das taxas de alfabetização e proporção de pessoas sem instrução ou com fundamental completo na categoria de sexo. O resumo também é alterado conforme os filtros selecionados, o tornando mais funcional. 
<br>

# 💬 Análise do Painel de Nível de Instrução 

## a) Comparação de resultados por Sexo 
<br>
  A taxa de alfabetização de homens é ligeiramente superior a de mulheres em 0,2 p.p na média dos 4 anos analisados. No caso de pessoas com fundamental incompleto (sem instrução) ou fundamental completo, a média da proporção de homens é 7,6 p.p 
<br>
<br>
<img width="280" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/477c530d-dda2-4174-b96b-d03c1d19dfb3">

## b) Comparação de resultados por Raça/Cor 
<br>
  No visão por Raça/Cor, é possível observar que a média da taxa de alfabetização é superior em 7,7 p.p para pessoas brancas. Para o cenário de pessoas com fundamental incompleto ou fundamental completo, o cenário se inverte e a média da proporção é de 37 p.p acima para pretos ou pardos. 
<br>
<br>
<img width="280" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/121d6a97-2b0f-484f-894a-e53a6aaa5adc">

## c) Comparação de resultados interseccionados 
<br>
  No painel estão disponíveis alguns "cards" que contém os big numbers para essa comparação. Sendo assim, a média da taxa de alfabetização para mulheres brancas é de 0,3 p.p acima da média da taxa de homens brancos alfabetizados. No caso de mulheres pretas ou pardas, a variação é de -0,8 p.p versus a média da taxa para homens pretos ou pardos. 

## d) Validação com pesquisa em literatura 
<br>
  Pela própria literatura são encontradas pesquisas que abordam uma disparidade entre os graus de escolaridade para homens e mulheres 
[1], e mesmo que para o caso de mulheres brancas versus homens brancos existir uma ligeira crescente por motivos de acesso à escola, não diminui o foco na desigualdade de acesso à escola para homens e mulheres.
  Como discutido desde a década de 90, os problemas estruturais na rede de ensino básico brasileira refletem em taxas como as de alfabetização de pessoas brancas versus pessoas pretas ou pardas, o que comprova tanto os problemas de estrutura quanto de falta de oportunidade que ainda atingem boa parte da população brasileira [2]. 
Nesse aspecto, algumas hipóteses podem ser levantadas [3]: 
<br>
<br>
<li> Lacuna em oportunidade de estudo para mulheres tendo em vista a associação à tarefas domésticas;
<li> Mercado de trabalho ainda privilegia e valoriza homens;
<li> Reflexo da estrutura brasileira de desigualdade racial;
<li> Concentração de analfabetos em faixas etárias superiores a 50 anos, considerando a falta de incentivo à formação no séc. XX;
<li> Cenário de ofertas de vagas e/ou rede escolar pública ainda em déficit versus a necessidade da população. 

**Um disclaimer que gostaria de adicionar:**
_Apesar dos dados serem até 2016 entende-se que muito dessa realidade ainda perdura até os dias atuais, por se tratar de um tópico muito pertinente foi realizada a análise por curiosidade sobre o tema também._


# Referências 
<br>
[1] Rosemberg, F.Educação e Gênero no Brasil. Proj.História, São, Paulo, 1994. Disponível em:https://revistas.pucsp.br/revph/article/download/11411/8316
<br>
[2] Rosemberg, F.; Piza, E. Analfabetismo, gênero e raça no Brasil. Revista USP, São Paulo, 1996. Disponível em: https://www.revistas.usp.br/revusp/article/download/28368/30226
<br>
[3] Haddad, S.; Silveira, F. Analfabetismo entre Jovens e Adultos no Brasil. Revista Brasileira de Alfabetização - ABALF, Espírito Santo, dez/2015. Disponível em: https://revistaabalf.com.br/index.html/index.php/rabalf/article/view/81/64



