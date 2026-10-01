# Análise de Viagens a Serviço - Governo Federal (2023)

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amandapereez/analise-viagens/blob/main/analise_viagens.ipynb)

Análise das despesas com viagens a serviço do Governo Federal em 2023, agrupadas por cargo público. 
> Projeto desenvolvido durante o curso **Python para Dados: do zero à análise completa**, da **Asimov Academy**, com foco na aplicação prática de Python e Pandas para tratamento, análise e visualização de dados públicos.

O notebook gera:

- Uma **tabela consolidada** por cargo (despesa média, duração média, despesas totais, destino mais frequente e número de viagens), salva em Excel;
- Um **gráfico** da despesa média por cargo, considerando apenas os cargos com mais de 1% das viagens.

![Despesa média em viagens por cargo público (2023)](output/grafico_2023.png)

> As barras estão ordenadas pelo **número de viagens** de cada cargo (de cima para baixo, do mais ao menos frequente), e não pelo valor da despesa média.

## Principais resultados

Valores aproximados, lidos do gráfico acima. A tabela consolidada, com os cargos que representam mais de 1% das viagens, está em [`output/tabela_2023.xlsx`](output/tabela_2023.xlsx).

- **Técnico do Seguro Social tem a maior despesa média por viagem**, em torno de R$ 4.300. É mais que o dobro da de cargos como Professor do Magistério Superior (cerca de R$ 2.000).
- **A despesa média varia bastante entre cargos**: de cerca de R$ 1.000 (Contratado Lei 8745/93) a mais de R$ 4.000.
- **Os dois grupos com mais viagens não são cargos de fato**: "Não identificado" e "Informações protegidas por sigilo". Ambos têm despesa média alta, perto de R$ 3.200. Isso mostra uma limitação dos dados: uma parte relevante das viagens não permite saber quem viajou.
- **Entre os cargos identificados**, Analista Ambiental (cerca de R$ 2.600) e Auditor-Fiscal da Receita Federal (cerca de R$ 2.400) aparecem logo depois dos primeiros colocados.

**Limitações:** a média por cargo pode ser puxada para cima por poucas viagens muito caras, como as internacionais. A análise não separa viagens nacionais e internacionais nem considera o motivo da viagem.

## Fonte dos dados

[Portal da Transparência do Governo Federal](https://portaldatransparencia.gov.br/) (Controladoria-Geral da União). São dados públicos.

O arquivo `2023_Viagem.csv` é grande demais para ser armazenado no GitHub. Por isso, o notebook baixa automaticamente uma cópia do arquivo disponibilizada no [Google Drive](https://drive.google.com/file/d/18j80hFqWkKMRyWGm_Jol539dX0Z0Vkoz/view).

## Como executar

**No Google Colab (1 clique):** clique no botão "Abrir no Colab" no topo desta página e execute as células. Os dados são baixados sozinhos.

**No seu computador:**
1. Instale as dependências: `pip install -r requirements.txt`
2. Execute o notebook `analise_viagens.ipynb`. Na primeira execução, ele cria a pasta `data/` e baixa automaticamente o CSV.

Os resultados são salvos na pasta `output/`.

## Estrutura

```
.
├── analise_viagens.ipynb
├── requirements.txt
└── output/
    ├── grafico_2023.png
    └── tabela_2023.xlsx
```

## Observações

- O CSV usa codificação `Windows-1252`, separador `;` e vírgula como separador decimal.
