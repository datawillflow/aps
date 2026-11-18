# Probabilidade Conjunta e Condicional do Baixo Peso ao Nascer — SINASC 2024

**Atividade Prática Supervisionada (APS) | Bacharelado em Estatística — FMU | 2026**

Estudo estatístico sobre a ocorrência de baixo peso ao nascer no Estado de São Paulo, com aplicação de conceitos de probabilidade simples, conjunta e condicional a partir dos microdados do Sistema de Informações sobre Nascidos Vivos (SINASC), referentes a 2024.

---

## 1. Sobre o projeto

Este projeto investiga como a probabilidade de um nascido vivo apresentar baixo peso varia segundo características maternas e gestacionais.

A análise utiliza registros de nascimentos de mães residentes no Estado de São Paulo em 2024 e aplica conceitos fundamentais da teoria das probabilidades para descrever associações entre baixo peso ao nascer, prematuridade, idade materna, consultas pré-natais, escolaridade, tipo de gravidez e sexo.

O trabalho integra a disciplina **Distribuições de Probabilidades e Probabilidades Conjuntas**, do segundo semestre do Bacharelado em Estatística da FMU.

### Objetivo

Calcular, interpretar e comunicar probabilidades de baixo peso ao nascer utilizando dados reais, explicitando em cada análise os eventos, numeradores, denominadores e significados dos resultados.

### Objetivos de Desenvolvimento Sustentável

**ODS 3 — Saúde e Bem-Estar**

O estudo possui relação contextual com a meta 3.2, voltada à redução das mortes evitáveis de recém-nascidos. O trabalho analisa o peso ao nascer como indicador de saúde materna e fetal, sem avaliar diretamente o cumprimento dessa meta.

---

## 2. Fonte de dados

**Fonte principal:** Sistema de Informações sobre Nascidos Vivos (SINASC), do Ministério da Saúde.

- Base: Microdados nacionais do SINASC 2024.
- Abrangência: Estado de São Paulo.
- Unidade de observação: Declaração de Nascido Vivo.
- Universo analisado: Nascimentos de mães residentes em São Paulo, ocorridos em 2024, com peso entre 300 g e 6.500 g.

**Portal oficial:**

https://dadosabertos.saude.gov.br/dataset/sistema-de-informacao-sobre-nascidos-vivos-sinasc

### Composição do universo

| Etapa | Registros |
|---|---:|
| SINASC 2024 — Brasil | 2.389.325 |
| Mães residentes em SP | 470.887 |
| Exclusão por peso fora do intervalo definido | 112 |
| **Universo final (Ω)** | **470.775** |
| Universo com idade gestacional classificada (ΩG) | 470.013 |

Os registros sem classificação de idade gestacional foram mantidos no universo geral, mas excluídos das análises que exigem essa variável.

---

## 3. Variáveis investigadas

| Variável | Categorias |
|---|---|
| Baixo peso ao nascer | Menos de 2.500 g / 2.500 g ou mais |
| Idade gestacional | Prematuro / 37 semanas ou mais |
| Idade materna | Até 19 / 20–34 / 35 anos ou mais |
| Consultas pré-natais | 0–3 / 4–6 / 7 ou mais |
| Escolaridade | Sem escolaridade até superior completo |
| Tipo de gravidez | Única / dupla / tripla ou mais |
| Sexo | Feminino / masculino |

Categorias ignoradas ou sem informação são preservadas quando metodologicamente possível, com identificação dos respectivos denominadores.

---

## 4. Fundamentação estatística

O projeto utiliza os seguintes conceitos estudados na disciplina:

- **Probabilidade simples:** ocorrência de baixo peso ao nascer.
- **Probabilidade complementar:** probabilidade de nascimento sem baixo peso.
- **Probabilidade conjunta:** ocorrência simultânea de baixo peso e prematuridade.
- **Probabilidade condicional:** ocorrência de baixo peso entre prematuros e não prematuros.
- **Independência:** avaliação da dependência entre baixo peso e prematuridade.
- **Lei da probabilidade total:** reconstrução da probabilidade geral a partir dos grupos de idade gestacional.
- **Teorema de Bayes:** inversão da condição entre baixo peso e prematuridade.
- **Distribuição de Bernoulli:** representação binária da ocorrência de baixo peso.
- **Distribuição binomial:** modelagem da quantidade de casos em grupos hipotéticos de nascimentos.

### Fórmulas fundamentais

Probabilidade simples:

P(A) = n(A) / n(Ω)

Probabilidade conjunta:

P(A ∩ B) = n(A ∩ B) / n(Ω)

Probabilidade condicional:

P(A | B) = P(A ∩ B) / P(B)

Independência:

P(A ∩ B) = P(A) × P(B)

Lei da probabilidade total:

P(A) = Σ P(A | Gᵢ) × P(Gᵢ)

Teorema de Bayes:

P(B | A) = [P(A | B) × P(B)] / P(A)

Distribuição binomial:

P(X = k) = C(n,k) × pᵏ × (1-p)ⁿ⁻ᵏ

---

## 5. Principais resultados

### Baixo peso ao nascer

Em 2024, foram identificados:

| Indicador | Resultado |
|---|---:|
| Nascimentos analisados | 470.775 |
| Registros com baixo peso | 47.345 |
| Probabilidade de baixo peso | **10,06%** |

Aproximadamente 1 em cada 10 nascidos vivos apresentou peso inferior a 2.500 g.

### Prematuridade e baixo peso

| Indicador | Probabilidade |
|---|---:|
| Baixo peso entre prematuros | **52,43%** |
| Baixo peso entre nascidos a termo | **4,08%** |
| Prematuros entre os bebês de baixo peso | **64,22%** |

A proporção de baixo peso entre prematuros foi aproximadamente 12,84 vezes a observada entre nascidos com 37 semanas ou mais.

### Consultas pré-natais

| Consultas | Baixo peso |
|---|---:|
| 0 a 3 | 25,72% |
| 4 a 6 | 20,74% |
| 7 ou mais | 7,81% |

A comparação padronizada por idade gestacional reduziu a diferença entre os grupos, demonstrando a importância de considerar a composição das populações comparadas.

### Outros resultados

O estudo também identificou:

- Diferenças na ocorrência de baixo peso segundo a idade materna.
- Associação entre escolaridade materna e proporção de baixo peso.
- Proporções elevadas em gestações múltiplas.
- Diferenças descritivas segundo o sexo do recém-nascido.
- Dependência estatística entre baixo peso e prematuridade.

Os resultados são descritivos. Não representam efeitos causais nem estimativas de risco individual.

---

## 6. Metodologia e processamento

O trabalho foi organizado em etapas de processamento e análise:

1. Obtenção dos microdados públicos do SINASC 2024.
2. Delimitação do universo de nascimentos de mães residentes em São Paulo.
3. Aplicação dos critérios de plausibilidade do peso ao nascer.
4. Tratamento e categorização das variáveis.
5. Construção das tabelas de frequências absolutas e relativas.
6. Cálculo das probabilidades simples, conjuntas e condicionais.
7. Aplicação da lei da probabilidade total e do teorema de Bayes.
8. Análise das distribuições de Bernoulli e binomial.
9. Auditoria das tabelas e dos cálculos.
10. Interpretação dos resultados.

### Auditoria estatística

As tabelas agregadas foram submetidas a 32 testes de consistência, todos aprovados.

Foram verificadas:

- Consistência das frequências absolutas.
- Correspondência entre numeradores e denominadores.
- Reconstrução das tabelas de contingência.
- Coerência entre probabilidades diretas e condicionais.
- Validação do teorema de Bayes.
- Validação da lei da probabilidade total.

---

## 7. Estrutura do repositório

A organização proposta para os arquivos do projeto é:

```text
aps/
│
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
│
├── docs/
│   ├── relatorio/
│   │   └── APS_Probabilidade_ODS3.pdf
│   └── referencias.md
│
├── data/
│   ├── README.md
│   └── processed/
│
├── src/
│   ├── extracao.py
│   ├── tratamento.py
│   ├── categorizacao.py
│   ├── probabilidades.py
│   └── auditoria.py
│
└── results/
    ├── tabelas/
    └── indicadores/
```

A estrutura será atualizada conforme os arquivos e scripts forem incorporados ao repositório.

---

## 8. Reprodutibilidade

Um dos entregáveis da atividade é um pipeline automatizado para executar o processamento dos microdados do SINASC 2024, incluindo tratamento, categorização estatística, cálculo das probabilidades e auditoria.

Os scripts, dependências e instruções de execução serão documentados neste repositório à medida que sua implementação for disponibilizada.

**Nota sobre os dados:** os microdados individuais não devem ser versionados neste repositório. A obtenção da base deve ser feita diretamente pelo portal oficial do Ministério da Saúde. Resultados agregados e arquivos de código poderão ser disponibilizados para permitir a reprodução das análises.

---

## 9. Limitações

As análises estão sujeitas às limitações dos registros administrativos utilizados, incluindo possíveis erros de preenchimento, campos sem informação e limitações na classificação da idade gestacional.

Outras limitações importantes:

- As comparações são descritivas e não estabelecem causalidade.
- Não foram realizados testes de hipóteses nem intervalos de confiança.
- Grupos pequenos exigem cautela na interpretação.
- A quantidade de consultas pré-natais é influenciada pela duração da gestação.
- Os resultados descrevem os nascimentos registrados em 2024 e não devem ser interpretados como previsões para outros períodos.

A reconstrução documentada no relatório auditou as tabelas agregadas, mas ainda requer a reexecução integral do processamento sobre os microdados para validar o pipeline completo.

---

## 10. Integrantes

**Bacharelado em Estatística — 2º semestre | FMU**

| Integrante | Registro Acadêmico |
|---|---|
| Francisco Aparecido | 2026100902 |
| Jéssica Cruz | 2026117807 |
| Kemily Silva | 2026111503 |
| Murilo Hoff | 2026109547 |
| Pedro Miguel | 2026107109 |
| William Rufino | 2026100478 |

**Disciplina:** Distribuições de Probabilidades e Probabilidades Conjuntas  
**Professor:** Antonio Carlos  
**Instituição:** Centro Universitário FMU  
**Ano:** 2026

---

## 11. Referências

As principais referências utilizadas na fundamentação teórica incluem:

- BLENCOWE, H. et al. (2019). *National, regional, and worldwide estimates of low birthweight in 2015, with trends from 2000*. The Lancet Global Health.
- HENRIQUES, L. B. et al. (2019). *Acurácia da determinação da idade gestacional no Sistema de Informações sobre Nascidos Vivos (SINASC)*. Cadernos de Saúde Pública.
- HERNÁNDEZ-DÍAZ, S.; SCHISTERMAN, E. F.; HERNÁN, M. A. (2006). *The birth weight paradox uncovered?* American Journal of Epidemiology.
- KILSZTAJN, S. et al. (2003). *Assistência pré-natal, baixo peso e prematuridade no Estado de São Paulo, 2000*. Revista de Saúde Pública.
- KOTELCHUCK, M. (1994). *An evaluation of the Kessner Adequacy of Prenatal Care Index and a proposed Adequacy of Prenatal Care Utilization Index*. American Journal of Public Health.
- KRAMER, M. S. (1987). *Determinants of low birth weight: methodological assessment and meta-analysis*. Bulletin of the World Health Organization.
- LEAL, M. C. et al. (2016). *Prevalence and risk factors related to preterm birth in Brazil*. Reproductive Health.
- OKWARAJI, Y. B. et al. (2024). *National, regional, and global estimates of low birthweight in 2020, with trends from 2000*. The Lancet.

A bibliografia completa encontra-se no relatório acadêmico.

---

**Projeto acadêmico desenvolvido para fins educacionais.**

Dados públicos | Métodos estatísticos | Reprodutibilidade | ODS 3 — Saúde e Bem-Estar
