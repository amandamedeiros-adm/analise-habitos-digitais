# Análise de Hábitos Digitais: Horas de Celular vs. Qualidade de Vida

**Autora:** Amanda Medeiros  
**Data:** Agosto/2026  
**Ferramentas:** SQL (SQL Server), Power BI, Excel, GitHub

---

## 📌 Sobre o Projeto

## 🚧 Status do Projeto

- ✅ Coleta e limpeza dos dados (SQL)
- ✅ Análise descritiva e regressão (SQL/Excel)
- ✅ Box plot e diagrama de dispersão (Excel)
- ⬜ Dashboard interativo (Power BI) – **em andamento**
- ⬜ Publicação do dashboard (Power BI Service)

**Previsão de conclusão:** [31 de agosto de 2026]

Este projeto tem como objetivo analisar a relação entre **horas de uso do celular** e a **percepção de qualidade de vida** de 50 respondentes. Os dados foram coletados por meio de um questionário aplicado no primeiro semestre de 2026, como parte das atividades da disciplina de **Análise Estatística** no mestrado em Administração da FEI (linha de pesquisa: Gestão da Tecnologia e Inovação).

A pergunta central da pesquisa foi:

> *"Existe relação entre o tempo gasto no celular e a forma como as pessoas percebem sua qualidade de vida?"*

---

## 🗂️ Estrutura do Repositório

```
analise-habitos-digitais/
│
├── README.md                       # Documentação principal do projeto
│
├── dados/
│   └── pesquisa_habitos.csv        # Dados brutos da pesquisa
│
├── sql/
│   ├── 01_criar_tabela.sql         # Criação da tabela no SQL Server
│   ├── 02_inserir_dados.sql        # Inserção dos dados
│   └── 03_analise_estatistica.sql  # Análise descritiva e regressão
│
├── powerbi/
│   └── dashboard_habitos.pbix      # Dashboard interativo no Power BI
│
└── imagens/
    ├── boxplot_pesquisa_hab.png                 # Box plots das variáveis
    └── dispersão_pesquisa_hab.png               # Diagrama de dispersão com reta de regressão
```


---

## 📊 Metodologia

### Variáveis Analisadas

| Variável | Tipo | Descrição |
|----------|------|-----------|
| **Horas de Celular (X)** | Independente | Número de horas por dia utilizando o celular |
| **Qualidade de Vida (Y)** | Dependente | Nota de 0 a 10 sobre percepção de qualidade de vida |

### Ferramentas Utilizadas

- **SQL Server Management Studio (SSMS)**: Criação da tabela, inserção dos dados e consultas para análise descritiva e regressão.
- **Power BI**: Criação de dashboards e visualizações interativas.
- **Excel**: Gráfico box plot e de dispersão.
- **GitHub**: Versionamento e documentação do projeto.

---

## 📈 Análise Descritiva

### Estatísticas Descritivas

| Indicador | Horas de Celular | Qualidade de Vida |
|-----------|------------------|-------------------|
| Média | 5.68 | 4.64 |
| Mediana | 5.00 | 4.00 |
| Mínimo | 1.00 | 0.00 |
| Máximo | 14.00 | 10.00 |
| Desvio Padrão | 3.21 | 2.89 |
| Variância | 10.30 | 8.35 |

### Interpretação

- A média de horas de celular foi de **5,68 horas por dia**, com grande variabilidade (desvio padrão de 3,21 horas).
- A percepção de qualidade de vida teve média **4,64** (em uma escala de 0 a 10), indicando uma avaliação ligeiramente abaixo do ponto médio.
- A mediana de qualidade de vida (4,0) foi menor que a média, sugerindo que alguns respondentes com notas mais altas puxaram a média para cima.

---

## 📉 Análise de Correlação e Regressão

### Correlação

- **Coeficiente de Correlação (R):** 0,4452
- **Classificação:** Correlação positiva moderada

### Regressão Linear

- **Equação da Regressão:**  
  `Qualidade de Vida = 1,064 + 0,0611 × (Horas de Celular)`

- **R² (Coeficiente de Determinação):** 0,1982

### Interpretação

- Para cada hora adicional de uso do celular, a qualidade de vida **aumenta em média 0,061 pontos** (na escala de 0 a 10).
- Apesar da correlação positiva, o R² de 0,1982 indica que **apenas 19,8%** da variação na qualidade de vida é explicada pelas horas de celular – ou seja, 80,2% dependem de outras variáveis.

---

## 🖼️ Visualizações

### Box Plot das Variáveis

![Box Plot](imagens/boxplot_pesquisa_hab.png)

*Gráfico 1: Distribuição das horas de uso do celular e da percepção de qualidade de vida.*

O gráfico box plot acima mostra a distribuição das respostas para as variáveis "Horas de Uso do Celular" e "Percepção de Qualidade de Vida".

A linha central de cada caixa representa a **mediana** (valor do meio). A caixa, por sua vez, contém os 50% dos dados centrais (do percentil 25 ao 75). 

**Principais observações:**
- A **mediana de horas de celular** é de aproximadamente **5 horas por dia**, com 50% dos respondentes variando entre 3 e 8 horas.
- A **mediana da qualidade de vida** é **4** (em uma escala de 0 a 10), com a maioria das notas concentradas entre 2 e 7.

Isso indica que, embora a maioria das pessoas use o celular por um período considerável (entre 3 e 8 horas), a percepção geral de qualidade de vida se mantém em um patamar baixo a moderado, sugerindo que outros fatores podem estar influenciando essa percepção mais do que o simples tempo de tela.

### Dashboard Interativo (Power BI)

![Dashboard](imagens/dashboard.png)

### Diagrama de Dispersão com Reta de Regressão

![Dispersão](imagens/dispersão_pesquisa_hab.png)

*Gráfico 2: Relação entre horas de uso do celular e percepção de qualidade de vida.*

O diagrama de dispersão mostra a relação entre as duas variáveis para cada respondente, com a reta de regressão indicando a tendência geral.

**Observações:**
- A equação da regressão estimada é: `Qualidade de Vida = 3,3801 + 0,0707 × (Horas de Celular)`.
- O coeficiente de determinação (R²) é de **0,0089**, indicando que menos de 1% da variação na qualidade de vida é explicada pelas horas de celular.
- A correlação é muito fraca (R = 0,094), sugerindo que, para esta amostra, o tempo de uso do celular não é um bom preditor da qualidade de vida percebida.
- A dispersão dos pontos ao redor da reta de regressão reforça essa conclusão: não há um padrão claro de relação linear entre as variáveis.

## 🔍 Conclusão

A análise revelou uma **correlação positiva moderada** entre horas de uso do celular e percepção de qualidade de vida. No entanto, o baixo R² sugere que outros fatores – como idade, escolaridade, rede social preferida e frequência de uso de outras tecnologias – podem ter maior influência sobre a qualidade de vida percebida.

Este projeto demonstrou minha capacidade de:

- Coletar, limpar e estruturar dados em SQL;
- Realizar análises descritivas e inferenciais;
- Criar visualizações interativas no Power BI;
- Documentar e comunicar resultados de forma clara e acessível.

Vale destacar que os dados foram submetidos a um processo de limpeza, com a correção de dois outliers identificados (valores 200 e 30, corrigidos para 2 e 3, respectivamente). Essa correção foi essencial para que os resultados refletissem com mais precisão o comportamento da amostra.

---

## 🚀 Próximos Passos

- Incluir mais variáveis no modelo (ex: idade, escolaridade, rede social preferida);
- Aplicar técnicas de Machine Learning para prever qualidade de vida;
- Ampliar a amostra para aumentar a representatividade dos resultados.

---

## 📬 Contato

- **LinkedIn:** [linkedin.com/in/amanda-me](https://linkedin.com/in/amanda-me)  
- **E-mail:** medeirosamanda.mail@gmail.com  
- **GitHub:** [github.com/amandamedeiros-adm](https://github.com/amandamedeiros-adm) 

---

**Agradecimentos:** Este projeto foi desenvolvido como parte do mestrado em Administração na FEI, sob orientação da Prof.ª Dr.ª Aline Mariane de Faria, na linha de pesquisa em Gestão da Tecnologia e Inovação.
