# Análise Estatística do Campeonato Brasileiro (2012-2024)

Este repositório contém uma base de dados limpa com resultados das partidas do Campeonato Brasileiro (Série A) das temporadas de 2012 a 2024, além de odds pré-jogo fornecidas pelas casas de apostas.

---

## 📂 Arquivos Disponíveis

- `dados_campeonato_brasileiro_limpo.csv`:  
  Contém jogos limpos (sem linhas faltantes) e colunas relevantes para análise, incluindo gols, resultados e odds pré-jogo.

## Estrutura dos Dados

| Coluna    | Descrição                                   |
|-----------|---------------------------------------------|
| Country   | País da competição (sempre "Brazil")        |
| League    | Liga da competição (ex.: Serie A)           |
| Season    | Temporada do jogo (ano)                     |
| Date      | Data do jogo (formato dd/mm/yyyy)           |
| Time      | Horário do jogo                             |
| Home      | Time mandante                               |
| Away      | Time visitante                              |
| HG        | Gols do mandante                            |
| AG        | Gols do visitante                           |
| Res       | Resultado da partida (H=Casa, D=Empate, A=Visitante)|
| PSCH      | Odd pré-jogo para vitória do mandante       |
| PSCD      | Odd pré-jogo para empate                    |
| PSCA      | Odd pré-jogo para vitória visitante         |
| MaxCH/MaxCD/MaxCA | Odds máximas disponíveis no mercado  |
| AvgCH, AvgCD, AvgCA | Odds médias do mercado            |

## Objetivos do Repositório

- Fornecer uma base de dados consistente e limpa para estudos estatísticos e de machine learning no contexto do futebol brasileiro.
- Apoiar atividades práticas de ensino envolvendo:
  - Programação Orientada a Objetos (POO) em Python.
  - Análise estatística básica (média, regressão linear, comparações de odds).
  - Manipulação de estruturas de dados em Python (listas, dicionários, DataFrames).

## Como usar os dados (exemplo rápido)

```python
import pandas as pd

# Carregar os dados limpos
dados = pd.read_csv('dados_campeonato_brasileiro_limpo.csv')

# Conferir os dados carregados
print(dados.head())
print(f"Quantidade de jogos: {dados.shape[0]}")
