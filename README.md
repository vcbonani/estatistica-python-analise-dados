# 📊 Estatística com Python: Resumindo e Analisando Dados

Repositório com os estudos e o projeto prático do curso Estatística com Python: Resumindo e analisando dados, da Alura, parte da formação em Estatística para Ciência de Dados.

O curso trabalha os fundamentos da **estatística descritiva** aplicados com Python, cobrindo desde a identificação dos tipos de dados até medidas de tendência central, separatrizes e dispersão — sempre com foco em como esses conceitos apoiam a geração de insights e a tomada de decisão orientada a dados.

## 🎯 Objetivos do curso

- Aplicar conceitos básicos de estatística para gerar insights e resolver problemas de negócio
- Diferenciar tipos de dados (qualitativos nominais/ordinais, quantitativos discretos/contínuos) e tratá-los adequadamente
- Calcular e interpretar medidas de tendência central, separatrizes e dispersão
- Analisar a distribuição dos dados e o que seus comportamentos indicam
- Usar Python como ferramenta de suporte para decisões baseadas em dados

## 📁 Notebooks do repositório

| Notebook | Descrição |
|---|---|
| [`Estatística_com_Python_frequencias_e_medidas.ipynb`](./Estatística_com_Python_frequencias_e_medidas.ipynb) | Notebook de estudos com todas as demandas resolvidas ao longo das 5 aulas do curso |
| [`Desafios_-_Estatística.ipynb`](./Desafios_-_Estatística.ipynb) | Projeto prático: análise descritiva de dados reais da PNAD 2015 (IBGE) |

---

## 📚 Estatística com Python: frequências e medidas

Notebook de estudos construído em torno de um cenário de consultoria de dados para uma rede de varejo, respondendo a demandas reais de dois times: **marketing/vendas** (perfil de clientes, avaliações, tempo de entrega) e **RH/financeiro** (remuneração e equidade salarial).

### Aula 1 — Entendendo os dados
Classificação das variáveis da base de vendas em **qualitativas** (nominais e ordinais) e **quantitativas** (discretas e contínuas) — por exemplo, categoria do produto (nominal), avaliação do cliente (ordinal), quantidade de itens (discreta) e tempo de entrega (contínua) — como base para escolher a técnica estatística correta em cada análise.

### Aula 2 — Identificando o perfil do público
- **Avaliações dos clientes:** distribuição de frequência mostrou mais avaliações positivas que negativas, mas com volume relevante de notas "Péssimo", sinalizando pontos de atenção para o time de marketing.
- **Avaliações por região (tabela de contingência):** Centro-Oeste e Nordeste concentraram as melhores avaliações (+55% positivas); a Região Sul se destacou negativamente, com ~34% de avaliações ruins e quase 20% em "Péssimo".
- **Ticket médio por sexo e região:** homens gastam mais nas regiões Centro-Oeste e Nordeste (~R$150 de diferença); mulheres gastam mais no Sul e Sudeste (~R$300 de diferença) — insumo direto para segmentação de campanhas.

### Aula 3 — Analisando a tendência dos dados
- **Tempo de entrega por categoria (média):** identificação de categorias com maior gargalo logístico.
- **Vendas de eletrônicos no Nordeste (mediana vs. média):** a mediana (~R$2.990) se mostrou mais representativa que a média (~R$3.970), puxada para cima por vendas de alto valor.
- **Moda em campanha de livros:** distribuição bimodal na quantidade de livros comprados, sugerindo testar duas ofertas promocionais diferentes.
- **Relação entre média, mediana e moda:** tempo de entrega segue distribuição normal simétrica no geral, mas se torna assimétrico à direita entre clientes com nota 5 — evidência de que entregas mais rápidas se associam a maior satisfação.

### Aula 4 — Investigando os dados dos colaboradores
- **Histograma de salários (Regra de Sturges):** mais de 52% dos colaboradores concentrados na primeira faixa salarial (R$1.890–R$4.080); distribuição assimétrica à direita, como esperado em folhas salariais.
- **Quartis/percentis:** confirmação de que os salários de coordenadores estão entre o 1% mais alto da empresa.
- **Classificação por idade:** identificação dos 20% colaboradores mais jovens (2.218 pessoas) para um programa de aceleração de carreira.
- **Boxplot por sexo:** mediana salarial feminina abaixo de R$4.000 contra uma mediana masculina acima desse valor — insight levado ao RH para investigar equidade salarial.

### Aula 5 — Analisando as variações dos dados
- **Desvio médio absoluto (Inteligência Comercial x Consultoria de Vendas):** médias e medianas próximas entre os dois cargos, mas dispersão ligeiramente maior entre consultores — sugerindo revisão de critérios salariais.
- **Variância e desvio padrão (Estoquista x Repositor):** cargo de Estoquista com maior variância/desvio padrão, indicando inconsistência salarial que pode refletir méritos individuais ou falhas na política de remuneração.

---

## 🚀 Projeto: análise descritiva PNAD 2015 (IBGE)

O notebook **`Desafios_-_Estatística.ipynb`** aplica os mesmos conceitos a uma base real: uma adaptação da **Pesquisa Nacional por Amostra de Domicílios (PNAD) 2015**, do IBGE, considerando apenas as **pessoas responsáveis pelo domicílio**, com variáveis como UF, sexo, idade, cor/raça, anos de estudo, renda e altura.

> 📁 Fonte dos dados: [IBGE — Pesquisa Nacional por Amostra de Domicílios](https://www.ibge.gov.br/estatisticas/sociais/populacao/9127-pesquisa-nacional-por-amostra-de-domicilios.html?edicao=9128)

Principais etapas e conclusões da análise:

- **Aula 1:** exploração inicial da base (tipos de dados, distribuição por UF, conversão de `Sexo`, `Cor` e `Anos de Estudo` para variáveis categóricas) e identificação da renda mínima e máxima da amostra.
- **Aula 2 — perfil por sexo e cor:** homens pardos são o grupo mais frequente entre as pessoas responsáveis pelo domicílio, seguidos por homens brancos; entre mulheres, pardas e brancas aparecem em proporções próximas. Pessoas indígenas e amarelas somam menos de 1% da amostra em ambos os sexos. Na análise de renda média cruzando sexo e cor, o grupo de cor amarela apresenta a maior renda média em ambos os sexos, enquanto homens indígenas têm a menor renda média — já entre as mulheres, a menor renda média está no grupo preto/pardo.
- **Aula 3 — tendência central da renda:** cálculo de média, mediana e moda da renda, ranking dos Top 5 estados por renda média, e comparação das distribuições de altura e idade com suas respectivas medidas de tendência central.
- **Aula 4 — medidas separatrizes:** número de classes pela Regra de Sturges, histograma de renda até R$15.000, percentual de responsáveis ganhando até 1 salário mínimo (R$788 em 2015), faixa de renda dos 95% e do 1% mais bem pago, e boxplots de renda por sexo e cor.
- **Aula 5 — dispersão da renda:** desvio médio absoluto, variância e desvio padrão da renda geral, e comparações de dispersão salarial por anos de estudo, sexo e região Centro-Oeste.

## 🛠️ Tecnologias utilizadas

- **Python**
- **Pandas** e **NumPy** — manipulação e análise dos dados
- **Matplotlib** e **Seaborn** — visualização de dados (histogramas, boxplots, gráficos de densidade)
- **Jupyter/Google Colab** — ambiente de desenvolvimento

## 📌 Sobre mim

Sou Vinícius Cunha, Analista de Dados/BI com background em consultoria de Finanças Corporativas e Oracle EPM. Este repositório faz parte da minha jornada de aprofundamento em estatística e análise de dados com Python.

🔗 [LinkedIn](https://www.linkedin.com/in/viniciuscunhadata/) · [GitHub](https://github.com/vcbonani)
