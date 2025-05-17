# Basic Education Level Dashboard in Brazil

## Context
IBGE (Brazilian Institute of Geography and Statistics) is one of the largest information providers in the country.
In addition to offering an API resource for open data consumption, it is also possible to find other data resulting from research and statistical analyses conducted by the Institute.
<br>
For this project, data from 2012–2016 was used, covering literacy and other education levels such as elementary and high school, with a focus on analyzing diversity.

## 💻 Information
The following tools were used in this project:
<br>

<li> Excel: https://www.microsoft.com/pt-br/microsoft-365/excel </li> 
<li> Power BI: https://powerbi.microsoft.com/ </li> 
<li> IBGE Portal: https://www.ibge.gov.br/acesso-informacao/estatisticas.html </li> 
<br> [Data Sources] The data is available and processed in this same repository, saved in a CSV file.

## Objectives
The two main objectives of this project are to build a management dashboard and conduct analyses to generate insights from the available data.

### Construction of the Education Level Dashboard

#### 1) Data Cleaning + Import to Power BI
The data was available in spreadsheet format on the IBGE website. Rows were converted into columns and column names were standardized to make data consumption easier. Then, the file was saved as CSV and imported into Power BI.

#### 2) Relationships in Power BI
The Star Schema model was applied, built from 2 fact tables (event tables) and 3 dimension tables based on Race/Color, Gender, and Time. These dimensions are analyzed simultaneously across both fact tables. The model is shown in the image below:
<br><br>
<img width="500" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/843607a3-34ce-435a-8eca-97c2c23bfd7d">

#### 3) Measures Table
As the project prioritized analyzing average literacy rates and proportions, a dedicated table of measures was created and strategically used in the dashboard. The measures were also segmented to ensure intersectional analysis, covering categories such as: white women, Black or Brown women, white men, and Black or Brown men. As shown at the start of the dashboard in the image below:
<br><br>
<img width="500" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/73e74bd8-0b6a-4558-98c8-3bd94da9dc59">

#### 4) Filters
The main filters applied to the analyses correspond to the dimensions shared by the two fact tables. Thus:
<br><br>
<img width="150" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/312cceb6-319e-4842-bfc9-d3a97b9513ca">

#### 5) Smart Summary
Power BI’s Smart Narrative feature was also used to summarize key insights from the dashboard views. For example, comparing literacy rates and the proportion of people without education or with completed elementary education by gender was highlighted. The summary also dynamically updates based on selected filters, enhancing functionality.
<br>

### 💬 Dashboard Analysis of Education Levels

#### a) Gender-Based Comparison
<br> On average across the 4 years analyzed, men had a slightly higher literacy rate than women by 0.2 percentage points. 
For those with incomplete elementary education (no schooling) or completed elementary, the average male proportion was 7.6 percentage points higher. 

<br><br> <img width="280" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/477c530d-dda2-4174-b96b-d03c1d19dfb3">

#### b) Race/Color-Based Comparison
<br> From the Race/Color perspective, the average literacy rate for white people was 7.7 percentage points higher. 
However, for those with incomplete or completed elementary education, the situation is reversed — the average proportion was 37 percentage points higher for Black or Brown individuals. 

<br><br> <img width="280" alt="image" src="https://github.com/vitcuellar/Dados_Nivel_Instrucao_Basica_IBGE/assets/146594135/121d6a97-2b0f-484f-894a-e53a6aaa5adc">

#### c) Intersectional Comparison
<br> The dashboard includes “cards” displaying big numbers for these comparisons. 
For example, the average literacy rate for white women was 0.3 percentage points higher than that of white men. 
For Black or Brown women, the rate was 0.8 percentage points lower than for Black or Brown men.

#### d) Validation with Literature Review
<br> The literature includes studies highlighting disparities in education levels between men and women [1]. Even if white women show a slight upward trend compared to white men due to better school access, this does not negate the broader gender inequality in access to education. Since the 1990s, structural issues in Brazil’s basic education system have been reflected in literacy rates, especially the disparities between white and Black/Brown populations, demonstrating both infrastructural problems and lack of opportunity that still affect a large portion of Brazilians [2]. Some hypotheses can be raised [3]: <br><br> <li> Gaps in educational opportunities for women due to association with domestic tasks; <li> Labor market still favors and values men; <li> Reflection of Brazil’s structural racial inequality; <li> High illiteracy rates among people aged 50+, considering the lack of educational incentives in the 20th century; <li> Ongoing shortage of public school availability versus population needs.


#### Disclaimer:
Even though the data only goes up to 2016, much of this reality is still relevant today. Given the importance of the topic, the analysis was conducted out of curiosity as well.

# References
<br> [1] Rosemberg, F. *Education and Gender in Brazil.* Proj.História, São Paulo, 1994. Available at: https://revistas.pucsp.br/revph/article/download/11411/8316 
<br> [2] Rosemberg, F.; Piza, E. *Illiteracy, Gender, and Race in Brazil.* Revista USP, São Paulo, 1996. Available at: https://www.revistas.usp.br/revusp/article/download/28368/30226 
<br> [3] Haddad, S.; Silveira, F. *Illiteracy among Youth and Adults in Brazil.* Brazilian Literacy Journal – ABALF, Espírito Santo, Dec/2015. Available at: https://revistaabalf.com.br/index.html/index.php/rabalf/article/view/81/64
