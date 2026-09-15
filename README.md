# Análise Exploratória e Previsão de Demanda — Bike Sharing Dataset

Este repositório contém um projeto prático de **Ciência de Dados e Machine Learning** desenvolvido para analisar e prever a demanda por aluguel de bicicletas a partir de dados operacionais e meteorológicos.

O projeto foi construído no contexto de aprendizado em tratamento de dados, análise exploratória (EDA), visualização estatística e modelagem preditiva de regressão.

---

## 🎯 Objetivos do Projeto

- **Tratamento e Auditoria de Dados**: Inspeção de tipos, verificação de consistência e junção de variáveis explicativas e alvo.
- **Análise Exploratória (EDA)**: Investigação do comportamento dos usuários sob diferentes perspectivas de negócio:
  - Impacto da sazonalidade e estações do ano na demanda.
  - Variação entre dias úteis, finais de semana e feriados.
  - Correlação entre temperatura/sensação térmica e volume de aluguéis.
  - Influência das condições climáticas adversas (chuva, neve, névoa).
  - Padrão horário da demanda (picos de deslocamento trabalho/estudo vs. lazer).
- **Modelagem Preditiva (Machine Learning)**:
  - Treinamento e comparação de modelos de regressão: **Regressão Linear** e **Random Forest Regressor**.
  - Avaliação de desempenho com métricas estatísticas: **MAE (Mean Absolute Error)** e **R² (Coeficiente de Determinação)**.
  - Visualização de valores reais vs. valores previstos.
  - Simulação de tomada de decisão para cenários operacionais específicos.

---

## 📁 Estrutura do Diretório

```text
BikeSharing/
├── bike_sharing_analise_preditiva.ipynb   # Caderno Jupyter com toda a análise e modelos
├── pyproject.toml                         # Configuração do projeto e dependências (uv)
├── requirements.txt                       # Dependências em formato pip tradicional
├── .python-version                        # Versão do Python utilizada (3.12)
├── .gitignore                             # Regras de exclusão do Git
└── README.md                              # Documentação do projeto
```

---

## 📊 Dataset Utilizado

Os dados são obtidos diretamente do repositório da Universidade da Califórnia em Irvine (**UCI Machine Learning Repository**) por meio da biblioteca `ucimlrepo`:

- **Nome**: Bike Sharing Dataset
- **ID UCI**: 275
- **Referência**: Fanaee-T, H. (2013). *Bike Sharing Dataset*. UCI Machine Learning Repository. [DOI: 10.24432/C5W894](https://doi.org/10.24432/C5W894)

O conjunto de dados contém registros horários e diários de aluguel de bicicletas do sistema Capital Bikeshare em Washington D.C. (anos de 2011 e 2012), associados a condições climáticas e sazonais.

---

## 🚀 Como Configurar o Ambiente e Executar

Este projeto utiliza o [**uv**](https://docs.astral.sh/uv/) como gerenciador de ambientes e dependências Python, garantindo instalações rápidas e reprodutíveis.

### 1. Pré-requisitos
- Python 3.12 ou superior instalado (ou instalado automaticamente pelo `uv`).
- `uv` instalado. Se ainda não tiver:
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

### 2. Clonar o repositório e entrar na pasta
```bash
git clone <URL_DO_SEU_REPOSITORIO>
cd BikeSharing
```

### 3. Sincronizar o ambiente com uv
Basta executar um comando para criar a `.venv` e instalar todas as dependências:
```bash
uv sync
```

*(Opcional - via pip convencional)*:
```bash
python -m venv .venv
source .venv/bin/activate  # No Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### 4. Executando o Notebook
- **No VS Code / Cursor**: Abra o arquivo `bike_sharing_analise_preditiva.ipynb`, clique em **Select Kernel** no canto superior direito e selecione o interpretador da pasta `.venv`.
- **Via Jupyter**:
  ```bash
  uv run jupyter lab
  ```
  ou
  ```bash
  uv run jupyter notebook
  ```

---

## 🛠️ Tecnologias e Bibliotecas

- [Python 3.12](https://www.python.org/)
- [uv](https://docs.astral.sh/uv/) — Gerenciador de projetos e pacotes
- [Pandas](https://pandas.pydata.org/) — Manipulação e estruturação de dados
- [NumPy](https://numpy.org/) — Operações numéricas e vetoriais
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/) — Visualização estática e estatística de dados
- [Scikit-Learn](https://scikit-learn.org/) — Algoritmos de Machine Learning e métricas de regressão
- [ucimlrepo](https://github.com/uci-ml-repo/ucimlrepo) — Acesso direto aos datasets da UCI
