# Análise de Viagens a Serviço - Governo Federal (2023)

Análise das despesas com viagens a serviço do Governo Federal em 2023, agrupadas por cargo público. O notebook gera:

- uma **tabela consolidada** por cargo (despesa média, duração média, despesas totais, destino mais frequente e número de viagens), salva em Excel;
- um **gráfico** da despesa média por cargo, considerando apenas os cargos com mais de 1% das viagens.

## Fonte dos dados

[Portal da Transparência do Governo Federal](https://portaldatransparencia.gov.br/) (Controladoria-Geral da União), seção **Download de dados > Viagens**. São dados públicos.

O arquivo bruto **não está neste repositório** por ser grande demais para o GitHub.

## Como executar

1. Clone o repositório e instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
2. Baixe os dados de viagens de **2023** no Portal da Transparência, extraia o `.zip` e coloque o arquivo `2023_Viagem.csv` dentro da pasta `data/`.
3. Abra e execute o notebook:
   ```bash
   jupyter notebook analise_viagens.ipynb
   ```
4. Os resultados são salvos na pasta `output/` (`tabela_2023.xlsx` e `grafico_2023.png`).

## Estrutura

```
.
├── analise_viagens.ipynb
├── requirements.txt
├── data/        # coloque aqui o 2023_Viagem.csv (ignorado pelo Git)
└── output/      # tabela e gráfico gerados (ignorado pelo Git)
```

## Observações

- O CSV usa codificação `Windows-1252`, separador `;` e vírgula como separador decimal.
