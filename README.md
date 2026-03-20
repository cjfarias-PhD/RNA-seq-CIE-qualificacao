# RNA-seq-CIE-qualificacao
# Relatório de Controle de Qualidade — RNA-seq CIE vs AIR
## Análise de expressão gênica em amígdala de camundongos C57BL/6J

Este repositório contém o relatório consolidado de controle de qualidade 
gerado pelo MultiQC para o projeto de RNA-seq bulk descrito na dissertação.

---

## Visualizar o relatório

[🔗 Clique aqui para visualizar o MultiQC Report](https://htmlpreview.github.io/?https://github.com/cjfarias-PhD/RNA-seq-CIE-qualificacao/blob/main/multiqc_report.html)

---

## O que avaliar no relatório

### 1. Qualidade das leituras brutas (FastQC)
- **Phred score por base** → escore médio ≥ Q30 ao longo de todo o read
- **Conteúdo GC** → distribuição aproximadamente normal, centrada em ~50%
- **Sequências duplicadas** → valores elevados em RNA-seq são esperados
- **Adaptadores residuais** → ausentes ou mínimos após trimagem

### 2. Trimagem (Trimmomatic)
- **% reads sobreviventes** → espera-se retenção ≥ 90% dos reads

### 3. Alinhamento ao genoma de referência (STAR / GRCm39)
- **Taxa de alinhamento total** → espera-se ≥ 75%; neste estudo: média **97,8%**
- **Reads unicamente mapeados** → espera-se ≥ 70%; neste estudo: média **91,9%**
- **Reads multimapeados** → aceitável < 10%; neste estudo: média **5,85%**
- **Reads não mapeados** → aceitável < 10%; neste estudo: média **2,14%**

### 4. Consistência entre amostras
- As amostras devem apresentar métricas homogêneas entre si
- Amostras com desvios expressivos devem ser avaliadas com cautela

---

## Amostras

| Grupo | IDs |
|---|---|
| CIE (*Chronic Intermittent Ethanol*) | CIE_3, CIE_4, CIE_5, CIE_6 |
| AIR (controle) | AIR_10, AIR_11, AIR_12, AIR_13 |

---

## Informações técnicas

| Parâmetro | Detalhe |
|---|---|
| Plataforma | Illumina NextSeq 2000 |
| Tipo de leitura | Paired-end 2×100 pb |
| Kit de biblioteca | Illumina Stranded mRNA Prep, Ligation |
| Genoma de referência | GRCm39 / Ensembl release 109 |
| Alinhador | STAR |
| Sequenciamento realizado por | SELA — Rede PREMiUM |
