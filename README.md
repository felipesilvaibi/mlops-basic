# mlops-basic

Projeto básico de MLOPS para fins didáticos (fonte: [Medium MLOPS End-to-End](https://medium.com/@shanakachathuranga/end-to-end-machine-learning-pipeline-with-mlops-tools-mlflow-dvc-flask-heroku-evidentlyai-github-c38b5233778c))

## Ferramentas utilizadas

*   **Cookiecutter:** Estrutura do projeto de ciência de dados

*   **Controle de versão de dados (DVC):** Controle de versão dos ativos de dados e pipeline de dados

*   **Github:** Controle de versão de código

*   **Github Actions:** Pipeline CI-CD

*   **MLFlow:** Registro de modelo de Machine Learning

*   **Heroku:** Aplicativo (interface)

*   **Flask:** API (web service)

*   **EvidentlyAI:** Avaliação e monitoramento de modelos de ML em produção

*   **Pytest:** Testes unitários

## Principais Comandos

*   Criação e ativação de VIRTUAL ENV: `python3 -m venv env`, `source ./env/bin/activate`

*   Instalação das dependências: `pip install -r requirements.txt`

*   Disponibilização do servidor do MLFLOW: `mlflow server --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./artifacts --host 0.0.0.0 -p 1234`

*   Geração de nova versionamento com o DVC: `dvc repro`

*   Execução dos testes unitário com PYTEST: `pytest -v`

*   Criação de report de monitoração de Concept Drift com EvidentlyAI: `python3 src/models/model_monitor.py`

## Organização do projeto

    ├── LICENSE
    ├── Makefile           <- Makefile com comandos como `make data` ou `make train`
    ├── README.md          <- O README de nível superior para desenvolvedores que usam este projeto
    ├── data
    │   ├── external       <- Dados de fontes de terceiros
    │   ├── interim        <- Dados intermediários que foram transformados
    │   ├── processed      <- Conjuntos de dados canônicos finais para modelagem
    │   └── raw            <- O dump de dados original e imutável
    │
    ├── docs               <- Um projeto Sphinx padrão; veja sphinx-doc.org para detalhes
    │
    ├── models             <- Modelos treinados e serializados, previsões de modelos ou resumos de modelos
    │
    ├── notebooks          <- Jupyter Notebooks. A convenção de nomenclatura é um número (para ordenação),
    │                         as iniciais do criador e uma breve descrição delimitada por `-`, ex: `1.0-fds-exploracao-inicial-dados`
    │
    ├── references         <- Dicionários de dados, manuais e todos os outros materiais explicativos
    │
    ├── reports            <- Análise gerada como HTML, PDF, LaTeX, etc
    │   └── figures        <- Gráficos e figuras gerados para serem usados ​​em relatórios
    │
    ├── requirements.txt   <- O arquivo de requisitos para reproduzir o ambiente de análise, por exemplo,
    │                         gerado com `pip freeze > requirements.txt`
    │
    ├── setup.py           <- Torna o projeto pip instalável (pip install -e .) para que o src possa ser importado
    ├── src                <- Código fonte para uso neste projeto.
    │   ├── __init__.py    <- Torna src um módulo Python
    │   │
    │   ├── data           <- Scripts para baixar ou gerar dados
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts para transformar dados brutos em recursos para modelagem
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts para treinar modelos e, em seguida, usar modelos treinados para fazer previsões
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts para criar visualizações exploratórias e orientadas a resultados
    │       └── visualize.py
    │
    └── tox.ini            <- Arquivo tox com configurações para execução de tox; veja tox.readthedocs.io

***

Projeto baseado no template de data science [cookiecutter](https://drivendata.github.io/cookiecutter-data-science/). #cookiecutterdatascience
