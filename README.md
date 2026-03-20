# RNA-seq-CIE-qualificacao
# Relatório de Controle de Qualidade — RNA-seq CIE vs AIR
## Análise de expressão gênica em amígdala de camundongos C57BL/6J

Este repositório contém o relatório consolidado de controle de qualidade 
gerado pelo MultiQC para o projeto de RNA-seq bulk descrito na dissertação.

---

## Como visualizar o relatório

Acesse o relatório interativo pelo link:
[Clique aqui para visualizar o MultiQC Report](https://htmlpreview.github.io/?https://github.com/SEU_USUARIO/SEU_REPOSITORIO/blob/main/multiqc_report.html)

---

## O que avaliar no relatório

### 1. Qualidade das leituras brutas (FastQC)
- **Phred score por base** → espera-se escore médio ≥ Q30 ao longo 
  de todo o read
- **Conteúdo GC** → deve ser aproximadamente normal, centrado 
  em torno de 50%
- **Sequências duplicadas** → valores elevados em RNA-seq são 
  esperados e não necessariamente problemáticos
- **Adaptadores residuais** → devem estar ausentes ou em níveis 
  mínimos após trimagem

### 2. Trimagem (Trimmomatic)
- **% reads sobreviventes** → espera-se retenção de ≥ 90% dos reads
- **Reads descartados** → valores elevados podem indicar baixa 
  qualidade da biblioteca

### 3. Alinhamento ao genoma de referência (STAR / GRCm39)
- **Taxa de alinhamento total** → espera-se ≥ 75%; 
  neste estudo: média de 97,8%
- **Reads unicamente mapeados** → espera-se ≥ 70%; 
  neste estudo: média de 91,9%
- **Reads multimapeados** → valores aceitáveis < 10%; 
  neste estudo: média de 5,85%
- **Reads não mapeados** → valores aceitáveis < 10%; 
  neste estudo: média de 2,14%

### 4. Consistência entre amostras
- As amostras devem apresentar métricas homogêneas entre si
- Amostras com desvios expressivos em relação às demais 
  devem ser avaliadas com cautela

---

## Amostras
| Grupo | IDs |
|---|---|
| CIE (*Chronic Intermittent Ethanol*) | CIE_3, CIE_4, CIE_5, CIE_6 |
| AIR (controle) | AIR_10, AIR_11, AIR_12, AIR_13 |
