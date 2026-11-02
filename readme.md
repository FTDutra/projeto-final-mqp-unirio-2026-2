# Projeto Final — Método Quantitativo

**Universidade Federal do Estado do Rio de Janeiro (UNIRIO)**

- **Disciplina:** Método Quantitativo
- **Professor:** Marcio Barros
- **Alunos:** M.Sc. Renato Barreira; M.Sc. Frederico Thiers

Link do **repositório Google Colab**: https://colab.research.google.com/drive/1Gb-XAyO8iB68BbuoSy88KAMWGAhH0Yk-?usp=sharing

---

## 1. Sobre o projeto

Este repositório reúne os resultados computacionais obtidos a partir da execução dos algoritmos estudados no projeto, incluindo informações sobre os eventos ocorridos durante o processo de cálculo e as operações realizadas pelo algoritmo redutor de expressões regulares.

Os experimentos foram executados em **50 rodadas independentes**, numeradas de `0` a `49`, contemplando diferentes instâncias.

O objetivo da organização dos dados é permitir a análise dos resultados, a comparação entre execuções e a avaliação da qualidade das soluções encontradas.

## 2. Estrutura dos arquivos

Os resultados estão organizados em diretórios, sendo cada diretório correspondente a uma rodada de execução.

A estrutura geral do repositório segue o seguinte formato:

    projeto-final-mqp-unirio-2026-2/
    │
    ├── instances.csv
    │
    ├── 0/
    │   ├── instancia_1.csv
    │   ├── instancia_1_reducer.csv
    │   ├── instancia_2.csv
    │   ├── instancia_2_reducer.csv
    │   └── ...
    │
    ├── 1/
    │   ├── instancia_1.csv
    │   ├── instancia_1_reducer.csv
    │   └── ...
    │
    ├── ...
    │
    └── 49/
        ├── instancia_1.csv
        ├── instancia_1_reducer.csv
        └── ...

Cada diretório numerado representa uma rodada de execução e contém dois arquivos para cada instância:

1. **Arquivo da instância:** registra os eventos ocorridos durante o processo de cálculo.
2. **Arquivo da instância com sufixo `_reducer`:** registra as operações realizadas pelo algoritmo redutor de expressões regulares.

Além desses arquivos, o repositório contém o arquivo `instances.csv`, que reúne as informações gerais de todas as instâncias utilizadas nos experimentos.

## 3. Arquivos de resultados

### 3.1. Arquivo de eventos da instância

O arquivo identificado pelo nome da instância contém o histórico dos eventos ocorridos durante o processo de cálculo.

| Coluna | Descrição |
|---|---|
| `Index` | Índice da iteração em que ocorreu o evento. |
| `Event Name` | Nome do evento ocorrido. |
| `Regex` | Expressão regular resultante da aplicação do operador. |
| `Operator Name` | Tipo de operador aplicado. |
| `Arg for Operator` | Argumento aplicado ao operador. Não utilizado nas análises. |
| `Regex Origin` | Expressão regular anterior à aplicação do operador. |
| `Fitness` | Indicador de qualidade da expressão regular resultante. Quanto maior o valor, melhor a qualidade da solução. |

### 3.2. Arquivo de operações do redutor

O arquivo identificado pelo nome da instância acrescido do sufixo `_reducer` contém informações relacionadas à aplicação do algoritmo redutor de expressões regulares.

| Coluna | Descrição |
|---|---|
| `Event Name` | Nome do evento ocorrido. |
| `Operation Name` | Tipo de operação realizada pelo redutor. |
| `Index` | Índice da iteração em que ocorreu o evento. |
| `Node` | Transformação ocorrida. Não utilizado nas análises. |
| `Result Is Better` | Indica se a qualidade da solução melhorou após o evento. Valores vazios devem ser interpretados como `False`. |

## 4. Arquivo de instâncias — `instances.csv`

O arquivo `instances.csv` contém os dados gerais e as informações de referência de cada instância utilizada nos experimentos.

| Coluna | Descrição |
|---|---|
| `Instance` | Nome da instância. |
| `Matchlist` | Número de entradas na match list. |
| `Unmatchlist` | Número de entradas na unmatch list. |
| `Weight` | Peso da instância. |
| `Maxrank` | Maior valor possível para a qualidade da instância. |
| `Norvig` | Qualidade máxima atingida pelo algoritmo de Norvig. |
| `Bartolli` | Qualidade máxima atingida pelo algoritmo de Bartolli. |
| `Humans` | Qualidade máxima atingida por uma solução desenvolvida por humanos. |
| `Order` | Número de sequência utilizado para apresentação das instâncias nas tabelas. |

As informações de qualidade de Norvig, Bartolli e Humans servem como referências para a avaliação e comparação dos resultados obtidos nos experimentos.

## 5. Organização dos experimentos

Os experimentos estão distribuídos em 50 rodadas, numeradas de `0` a `49`.

Cada rodada contém os resultados individuais de todas as instâncias processadas, permitindo:

- Analisar o histórico de eventos de cada execução.
- Acompanhar a evolução da qualidade das expressões regulares.
- Avaliar as operações realizadas pelo algoritmo redutor.
- Comparar os resultados entre diferentes rodadas.
- Confrontar as soluções encontradas com os valores de referência disponíveis em `instances.csv`.

## 6. Observações sobre os dados

- Os valores de `Fitness` representam indicadores de qualidade, sendo que valores maiores indicam soluções melhores.
- Na coluna `Result Is Better`, valores vazios devem ser considerados equivalentes a `False`.
- As colunas `Arg for Operator` e `Node` são mantidas nos arquivos originais, mas não são utilizadas nas análises.
- A coluna `Order` deve ser utilizada para preservar a sequência definida de apresentação das instâncias nas tabelas.
