
# 📊 Projeto de ETL com Databricks e Azure via Kaggle

Este projeto tem como objetivo realizar um pipeline de ETL (Extração, Transformação e Carga) em uma base de dados obtida via Kaggle. Através da plataforma **Databricks Community Edition**, os dados são baixados e processados com dois notebooks principais: `data_ingestion` e `data_processing`.

## 🧩 Visão Geral

- **Extração**: Os dados são obtidos diretamente do Kaggle (via API), armazenados no Databricks DBFS e depois organizados em diretórios estruturados.
- **Transformação**: Aplicamos limpeza e tratamento dos dados para uso posterior.
- **Carga**: Os dados processados podem ser salvos no Azure Data Lake, SQL ou outro destino, conforme a extensão do projeto.

## 📁 Notebooks Utilizados

| Notebook         | Função                                                                 |
|------------------|------------------------------------------------------------------------|
| `data_ingestion` | Responsável por baixar os dados do Kaggle e armazená-los no DBFS       |
| `data_processing`| Realiza o processamento, limpeza e transformação dos dados extraídos   |

---

## 🚀 Como Usar Este Projeto

### 1. Clone este repositório
```bash
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
```

### 2. Faça login no [Databricks Community Edition](https://community.cloud.databricks.com/)

Crie uma conta gratuita se ainda não tiver.

---

### 3. Importe os notebooks

#### Opção A: Upload manual
1. No Databricks, vá até o menu lateral esquerdo → Workspace
2. Crie uma pasta com o nome do projeto
3. Clique com o botão direito na pasta → Import
4. Importe os arquivos `data_ingestion.py` e `data_processing.py` (ou `.ipynb`)

#### Opção B: Reimportar via `.dbc` (se disponível)
1. Vá em Workspace → Import
2. Importe o arquivo `.dbc` (Databricks Archive) diretamente

---

### 4. Configure sua conta Kaggle (API)
1. Acesse seu perfil no [Kaggle](https://www.kaggle.com/)
2. Vá em "Account" > "Create API Token"
3. Baixe o arquivo `kaggle.json`
4. No Databricks:
   - Vá em `Data` → `DBFS` → `/FileStore`
   - Faça o upload do arquivo `kaggle.json`
   - Configure no notebook o caminho: `/dbfs/FileStore/kaggle.json`

---

### 5. Execute os notebooks
1. Execute o `data_ingestion` primeiro
2. Depois execute o `data_processing`

---

## 📌 Requisitos

- Conta no [Kaggle](https://www.kaggle.com/)
- Conta no [Databricks Community Edition](https://community.cloud.databricks.com/)
- Permissão para upload no DBFS
- (Opcional) Conta no Azure para armazenar os dados processados

---

## 📬 Contato

Se tiver dúvidas ou quiser contribuir, fique à vontade para abrir uma *issue* ou *pull request*!
