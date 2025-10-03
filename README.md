# Análise de Perfil de Risco de Beneficiários - Unimed

## Descrição

Este repositório contém o projeto de extensão universitária desenvolvido em parceria com a **Unimed Ponta Grossa**, como parte das atividades acadêmicas da **UTFPR-PG (Universidade Tecnológica Federal do Paraná, campus Ponta Grossa)**.

O projeto consiste na análise de dados de beneficiários com o objetivo de construir um modelo de ciência de dados capaz de:

* **Identificar o perfil de risco** de beneficiários para o desenvolvimento de Doenças Crônicas Não Transmissíveis (DCNT).
* **Calcular o custo evitado** para pacientes que participam dos programas de acompanhamento da Unimed.
* **Gerar alertas** de possíveis candidatos a doenças crônicas que ainda não fazem parte dos programas de cuidado.

## Alunos

* **Arthur de Barros Marcondes Machado Rosisca**
* **Vinicius Fonseca Navarro**

## Contexto do Projeto

As doenças crônicas são um grande desafio para os sistemas de saúde. A identificação precoce e o acompanhamento de pacientes de risco podem levar a uma melhoria na qualidade de vida e a uma redução de custos para a operadora de saúde.

A Unimed Ponta Grossa possui programas de "Linha de Cuidado" para acompanhar beneficiários já identificados com DCNTs. O desafio proposto foi o de usar técnicas de Ciência de Dados para aprimorar esse processo, prevendo novos casos e medindo o impacto financeiro dos programas existentes.

## Estrutura do Repositório

O projeto está organizado nos seguintes diretórios e arquivos:

* `/AnaliseExplanatoria`: Contém o notebook `Projeto - Análise Exploratória.ipynb` com a análise exploratória inicial dos dados.
* `/Projeto Analise de Dados`: Contém o notebook `Projeto Ciencia de Dados.ipynb` com o desenvolvimento da análise, tratamento dos dados, criação de clusters de risco e visualizações.
* `/projetoFinal`: Contém o notebook `Projeto Final Document.ipynb` com a documentação final e conclusões do projeto.
* `/Dados`: Diretório (não incluído no repositório) onde os arquivos `.xlsx` com os dados brutos da Unimed foram armazenados para a análise.
* `/Resultados`: Diretório (não incluído no repositório) com os arquivos `.csv` e gráficos gerados durante a análise.

## Como Executar o Projeto

Para executar os notebooks e reproduzir a análise, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/projeto-unimed.git](https://github.com/seu-usuario/projeto-unimed.git)
    ```
2.  **Instale as dependências:**
    O projeto utiliza as seguintes bibliotecas Python:
    * pandas
    * numpy
    * os
    * datetime
    * scikit-learn
    * seaborn
    * matplotlib

    Você pode instalar todas com o pip:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib
    ```
3.  **Execute os Notebooks:**
    Abra e execute os notebooks Jupyter na seguinte ordem para um melhor entendimento do processo:
    1.  `AnaliseExplanatoria/Projeto - Análise Exploratória.ipynb`
    2.  `Projeto Analise de Dados/Projeto Ciencia de Dados.ipynb`
    3.  `projetoFinal/Projeto Final Document.ipynb`

## Metodologia

O projeto seguiu as seguintes etapas:

1.  **Carregamento e Limpeza dos Dados:** As diversas bases de dados fornecidas (atendimentos, beneficiários, procedimentos, etc.) foram carregadas e passaram por um processo de limpeza, tratando dados faltantes e corrigindo tipos de dados.
2.  **Análise Exploratória:** Foi realizada uma análise inicial para entender as características de cada conjunto de dados e identificar outliers.
3.  **Unificação e Engenharia de Features:** Os dados foram unificados em uma única base de dados mestre. Novas features, como IMC e faixas etárias, foram criadas para enriquecer a análise.
4.  **Modelagem (Clusterização):** Foi utilizado o algoritmo K-Means para agrupar os beneficiários em diferentes perfis de risco com base em suas características de idade, custo e utilização do plano.
5.  **Análise dos Perfis:** Os perfis gerados foram analisados e interpretados, resultando na identificação de grupos como "Críticos de Altíssimo Custo" e "Crônicos com Uso Frequente".
6.  **Modelagem (Classificação):** Um modelo de classificação (Random Forest) foi treinado para prever a probabilidade de um beneficiário ter DCNT, alcançando uma boa performance (AUC > 0.8).

## Conclusões

A análise permitiu a criação de um modelo preditivo funcional e a segmentação dos beneficiários em perfis de risco claros. Isso possibilita à Unimed direcionar ações de cuidado de forma mais eficiente, focando nos grupos de maior risco e potencial de custo, e, consequentemente, melhorando a saúde de seus beneficiários enquanto otimiza recursos.
