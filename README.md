# Análise de Sentimentos e Sumarização Inteligente de Avaliações de Produtos E-commerce

## 🎯 Visão Geral

Este projeto demonstra como modelos Transformer podem ser utilizados para a análise de dados não-estruturados em empresas de e-commerce. Utilizando técnicas de Processamento de Linguagem Natural (NLP), o sistema classifica automaticamente o sentimento de avaliações de produtos e gera resumos inteligentes, transformando grandes volumes de texto em insights acionáveis.

## 📋 Objetivos

- **Análise de Sentimentos**: Classificar automaticamente avaliações como positivas ou negativas
- **Sumarização Inteligente**: Gerar resumos concisos dos pontos fortes e fracos de produtos
- **Relatórios Automatizados**: Criar dashboards e relatórios para tomada de decisão

## 🏗️ Arquitetura Técnica

### Modelos Utilizados
- **BERTimbau** (neuralmind/bert-base-portuguese-cased): Modelo BERT específico para português brasileiro
- **mBART** (facebook/mbart-large-50-many-to-many-mmt): Modelo multilingue para sumarização

### Pipeline de Processamento
1. **Extração**: Download e carregamento do dataset B2W
2. **Pré-processamento**: Tokenização e formatação dos dados
3. **Fine-tuning**: Treinamento do modelo de sentimentos
4. **Análise**: Classificação de todas as avaliações
5. **Sumarização**: Geração de resumos por produto/categoria
6. **Relatórios**: Criação de insights acionáveis

## 📊 Dataset

**Fonte**: [ptbr-sentiment-analysis-datasets](https://www.kaggle.com/datasets/fredericods/ptbr-sentiment-analysis-datasets) (B2W)

**Características**:
- ~130k avaliações reais de e-commerce brasileiro
- Texto em português brasileiro nativo
- Labels binários: positivo (1) / negativo (0)
- Dados pré-processados e limpos

## 🚀 Instalação

### Pré-requisitos
- Python 3.12+
- pip
- Git

### Passos de Instalação

1. **Clone o repositório**:
```bash
git clone <repository-url>
cd product-review-analysis
```

2. **Crie um ambiente virtual**:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate     # Windows
```

3. **Instale as dependências**:
```bash
pip install -r requirements.txt
```

4. **Verifique a instalação**:
```python
python -c "import transformers, datasets, torch; print('Instalação bem-sucedida!')"
```

## 📖 Execução Completa
Abra o notebook Jupyter e execute todas as células sequencialmente:

```bash
jupyter notebook product-review-analysis.ipynb
```

## 📈 Resultados Esperados

### Métricas de Performance (Ainda não executadas)
- **Accuracy**: >85%
- **F1-Score**: >82%
- **AUC-ROC**: >90%

### Outputs do Sistema
- Relatórios Markdown por produto/categoria
- Estatísticas agregadas de satisfação
- Exemplos de avaliações positivas/negativas
- Recomendações automáticas baseadas nos dados


## 📁 Estrutura do Projeto

```
product-review-analysis/
├── product-review-analysis.ipynb    # Notebook principal
├── requirements.txt                 # Dependências
├── README.md                        # Este arquivo
├── best_sentiment_model/           # Modelo treinado (gerado)
├── results/                        # Checkpoints e logs
├── logs/                           # Logs de treinamento
└── report_*.md                     # Relatórios gerados
```

### Casos de Uso
- **Monitoramento de Produtos**: Alertas automáticos para produtos com baixa satisfação
- **Análise de Concorrência**: Comparação de performance entre produtos similares
- **Suporte ao Cliente**: Roteamento inteligente baseado no sentimento das avaliações
- **Marketing**: Identificação de pontos fortes para campanhas promocionais

## 📞 Autoria e Informação Acadêmica

**Autora:** Lara Linhares  
**Disciplina:** Redes Neurais Artificiais  
**Professor:** Denilson Pereira
**Instituição:** UFLA
**Ano:** 2025

---

**Nota**: Este é um projeto acadêmico demonstrativo. Para uso em produção, considere aspectos de segurança, escalabilidade e governança de dados.
