mlops-basic
==============================

Projeto básico de MLOPS para fins didáticos (fonte: [Medium MLOPS End-to-End](https://medium.com/@shanakachathuranga/end-to-end-machine-learning-pipeline-with-mlops-tools-mlflow-dvc-flask-heroku-evidentlyai-github-c38b5233778c))

Dependências Externas
----------
- python3 package
- pip package

Principais Comandos
-----------
- Criação e ativação de VIRTUAL ENV: `python3 -m venv venv | source /venv/bin/activate`
- Instalação das dependências: `pip install -r requirements.txt`
- Disponibilização do servidor do MLFLOW: `servidor mlflow --backend-store-uri sqlite:///mlflow.db --default-artifact-root ./artifacts --host 0.0.0.0 -p 1234`
- Geração de nova versionamento com o DVC: `dvc repro`
- Execução dos testes unitário com PYTEST: `pytest -v`

Organização do projeto
------------

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


--------

<p><small>Projeto baseado no modelo de projeto de ciência de dados <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter </a>. #cookiecutterdatascience</small></p>
