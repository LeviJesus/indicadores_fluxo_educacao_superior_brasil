# Indicadores de Fluxo da Educação Superior no Brasil

Este projeto visa analisar os indicadores de fluxo da educação superior no Brasil utilizando dados do INEP. O projeto inclui scripts para baixar, processar e visualizar os dados.

## Escopo da Análise

A análise é focada no acompanhamento dos ingressantes no ensino superior do ano de 2014 durante 10 anos, até 2023. Os dados incluem informações sobre taxas de permanência, conclusão, desistência e outros indicadores relevantes para entender o fluxo dos estudantes no ensino superior brasileiro.

Os dados são públicos e encontram-se disponíveis no site do INEP: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/indicadores-educacionais/indicadores-de-fluxo-da-educacao-superior

## Aplicativo Streamlit

Caso você não queira rodar o projeto localmente em sua máquina, você pode acessar o aplicativo Streamlit e interagir com ele, fazendo suas próprias análises através do link abaixo: 

https://indicadores-fluxo-educacao-superior-brasil.streamlit.app/

## Estrutura do Projeto

- `app/`
  - `streamlit_dashboard.py`: Interface de visualização dos dados utilizando Streamlit.
  - `data_loader.py`: Carrega e mapeia os dados para melhor entendimento.
- `assets/`
  - `inep.png`: Imagem usada no aplicativo Streamlit.
- `data/`
  - `raw/`: Contém os dados brutos baixados.
  - `processed/`: Contém os dados processados prontos para análise.
  - `database.db`: Base de dados criada no SQLite para análises e processamentos.
- `scripts/`
  - `db_manager.py`: Gerencia a conexão e operações com o banco de dados SQLite.
  - `data_processor.py`: Processa os dados brutos e os salva no banco de dados.
  - `data_downloader.py`: Baixa e extrai os dados do INEP.
- `main.py`: Script principal para executar o fluxo completo de download, processamento e armazenamento dos dados.

# Observações sobre o Projeto

A ideia de construir um banco de dados no SQLite é para analisar possíveis tendências nos dados e aplicar algoritmos de machine learning futuramente. Isso permitirá uma análise mais profunda e eficiente, além da criação de modelos preditivos baseados nos indicadores de fluxo da educação superior. 

Além disso, construir a base em SQLite nos permite rodar o app streamlit na nuvem sem precisar consumir um arquivo local pesado.

## Requisitos

- Python 3.8+
- Bibliotecas Python:
  - `pandas`
  - `sqlalchemy`
  - `requests`
  - `zipfile`
  - `streamlit`
  - `plotly`
  - `openpyxl`

## Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/LeviJesus/indicadores_fluxo_educacao_superior_brasil.git
   cd indicadores-fluxo-educacao-superior-brasil
   ```

2. Crie um ambiente virtual e instale as dependências:
   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows use `venv\Scripts\activate`
   pip install -r requirements.txt
   ```

## Uso

1. Execute o script principal para baixar, processar e armazenar os dados:
   ```bash
   python main.py
   ```

2. Inicie o dashboard do Streamlit para visualizar os dados:
   ```bash
   streamlit run app/streamlit_dashboard.py
   ```


## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.
