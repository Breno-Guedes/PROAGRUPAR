# PROAGRUPAR: Análise Preditiva e Detecção de Bloqueios em Redes Ópticas Elásticas

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

## Sobre o Projeto

O PROAGRUPAR é uma iniciativa de pesquisa e desenvolvimento científico liderada pela Coordenação do Curso de Análise e Desenvolvimento de Sistemas do IFPI Campus Corrente, sob a orientação do Professor Jurandir Cavalcante.

Este projeto insere-se no domínio das Redes Ópticas Elásticas (EONs - Elastic Optical Networks), uma tecnologia emergente fundamental para a próxima geração de telecomunicações devido à sua flexibilidade e eficiência espectral. O foco central deste estudo é o problema de Roteamento, Modulação, Espectro e Alocação de Núcleos (RMSCA), considerando as limitações impostas por fenômenos físicos degradantes, especificamente o Crosstalk (interferência entre núcleos em fibras multicore).

### Metodologia e Ferramentas

A pesquisa utiliza o simulador SNetS (Simulator for Network Slicing / Optical Networks), fornecido pelo coordenador do projeto, para a geração de bases de dados sintéticas que representam cenários realistas de tráfego de rede. O SNetS simula requisições de conexão e alocação de recursos, permitindo a análise de métricas críticas de desempenho.

O objetivo primordial deste repositório é aplicar e comparar técnicas de Aprendizado de Máquina (Machine Learning) para processar os dados gerados pelo SNetS. Busca-se identificar qual algoritmo oferece a maior acurácia na predição de bloqueios de rede, classificando se uma determinada requisição será aceita ou bloqueada com base nos parâmetros da rede e nas restrições de qualidade de sinal (QoT).

## Algoritmos Avaliados

O estudo realiza uma análise comparativa de desempenho entre seis algoritmos de aprendizado supervisionado para classificação:

1. Random Forest (Floresta Aleatória)
2. Naive Bayes
3. Decision Tree (Árvore de Decisão/Binária)
4. Logistic Regression (Regressão Logística)
5. Support Vector Machine (SVM - Máquina de Vetores de Suporte)
6. Artificial Neural Networks (ANN - Redes Neurais Artificiais)

## Estrutura do Repositório

A organização dos arquivos visa facilitar a reprodutibilidade dos experimentos e a colaboração entre os pesquisadores.

```
PROAGRUPAR/
│
├── data/
│   └── baseMLJurandir.zip                 # Conjunto de dados brutos gerados pelo simulador SNetS
│
├── notebooks/                             # Implementações dos modelos de Machine Learning
│   ├── lr_dt/                             # Regressão Logística e Árvore de Decisão
│   │   └── logistic_regression_and_decision_tree.ipynb
│   ├── rf_naive_bayes/                    # Random Forest e Naive Bayes
│   │   └── random_forest_and_naive_bayes.ipynb
│   └── svm_ann/                           # SVM e Redes Neurais Artificiais (ANN)
│       └── svm_and_neural_networks.ipynb
│
├── .gitattributes                         # Atributos e configurações de repositório do Git
├── .gitignore                             # Regras de exclusão de arquivos para o Git
└── README.md                              # Documentação técnica do projeto
```

## Instruções de Uso

### 1. Clonagem e Configuração do Ambiente

Para obter o código-fonte, recomenda-se clonar o repositório utilizando o Git:

```bash
git clone https://github.com/Breno-Guedes/PROAGRUPAR.git
cd PROAGRUPAR
```

Alternativamente, é possível baixar o repositório como um arquivo ZIP através da interface do GitHub e extraí-lo localmente.

### 2. Execução no Google Colab

Este projeto foi otimizado para execução em ambiente de nuvem via Google Colab. Siga os passos abaixo para garantir o funcionamento correto dos notebooks:

Carregamento dos Notebooks:
1. Acesse o Google Colab.
2. Navegue até "Arquivo" > "Abrir notebook".
3. Selecione a aba "GitHub", insira a URL deste repositório e escolha o notebook desejado.

Preparação dos Dados (Etapa Crítica):
Os notebooks dependem dos arquivos gerados pelo SNetS. Para que a execução ocorra sem erros:
1. No ambiente do Google Colab, abra o menu lateral esquerdo (ícone de pasta/arquivos).
2. Crie uma pasta denominada "data" na raiz do ambiente virtual.
3. Realize o upload dos arquivos de dados (ex: .csv, .xlsx) contidos na pasta "data" deste repositório para a pasta recém-criada no Colab.

### 3. Execução dos Experimentos

Ao abrir um notebook, recomenda-se seguir as boas práticas abaixo:

- Leitura Sequencial: Execute as células de código na ordem apresentada (de cima para baixo).
- Documentação Interna: Leia os comentários presentes no código para compreender as etapas de pré-processamento, treinamento e validação.
- Análise de Resultados: Verifique os outputs gerados, incluindo matrizes de confusão, relatórios de classificação e gráficos de desempenho.

## Contribuição e Manutenção

Para manter a integridade científica e a organização do projeto, solicita-se aos colaboradores que sigam as seguintes diretrizes:

- Versionamento: Utilize o Git corretamente, evitando o envio de arquivos temporários ou desnecessários (já configurados no .gitignore).
- Padronização: Mantenha a nomenclatura dos arquivos e a estrutura de pastas inalterada.
- Documentação: Comente trechos complexos de código e documente quaisquer alterações nos hiperparâmetros dos modelos.

## Contato

Para dúvidas relacionadas à metodologia, acesso ao simulador SNetS ou discussão dos resultados, entre em contato com a equipe PROAGRUPAR ou com o coordenador do curso no Campus Corrente.

Desenvolvido pela equipe PROAGRUPAR.
