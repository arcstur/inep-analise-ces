# INEP-CES
Análise dos microdados do Censo da Educação Superior do INEP

Por padrão a análise é feita para o curso de Arquitetura e Urbanismo, no estado do Rio Grande do Sul. Isso pode ser configurado com variáveis de ambiente.

## Dados

Os dados podem ser acessados [aqui](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/censo-da-educacao-superior). Porém, o programa faz o download deles automaticamente, então não é preciso baixá-los manualmente.

Utilizam-se os dados a partir de 2009 por possuírem a mesma estrutura de colunas.

## Instalação

Instale o [Python](https://www.python.org) e o [Poetry](https://python-poetry.org).

## Cálculo de concluintes por ano

Rode
```bash
poetry install
poetry run python concluintes.py
```
Os resultados são salvos na pasta `output/`.

## Configuração

As seguintes variáveis de ambiente definem o programa.
- `NO_CURSO` (default `ARQUITETURA E URBANISMO`): nome do curso, em caixa alta.
- `SG_UF` (default `RS`): sigla da UF
- `PLOT_ACTION` (default `EXPORT`): ação a realizar com os gráficos: `EXPORT` os salva e `SHOW` os mostra.
- `PYTHON_LOG` (default `INFO`): define o [nível do log](https://docs.python.org/3/howto/logging.html#when-to-use-logging) do `logging` do python
