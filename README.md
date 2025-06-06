# Relatório de Atividade - Indicadores Educacionais

**Universidade Federal Fluminense**  
**Instituto de Matemática e Estatística**  
**Departamento de Estatística**  
Prática Estatística 1  
1º semestre de 2025

## 👥 Autores

- Bruno Oliveira Alves dos Santos  
- Daniel Martins de Faria  
- Fernanda Alexandrina dos Santos  
- Fernando Lucas Santos de Oliveira  
- Pedro Truppel Duarte Xavier  
- Renato Guimarães Guerreiro

---

## 📘 Introdução

Este relatório tem como objetivo propor indicadores educacionais com base nos microdados do Censo Escolar da Educação Básica de 2024, disponibilizados pelo Inep. Essa base contempla informações sobre matrículas, corpo docente, turmas, infraestrutura e o perfil institucional das escolas brasileiras.

Os indicadores elaborados pelo grupo abordam aspectos como o acesso a computadores e internet, a proporção de escolas públicas e privadas, a presença de recursos de acessibilidade física e os tipos de esgotamento sanitário disponíveis nas instituições de ensino.

---

## 📊 Indicadores Propostos

Cada indicador é descrito com sua respectiva fórmula de cálculo e justificativa de escolha.



### 1. Proporção de Escolas Públicas e Privadas

```math
E_{j,\text{pública}} = E_{j,\text{federal}} + E_{j,\text{estadual}} + E_{j,\text{municipal}}

E_{j,\text{privada}} = \text{número de escolas privadas no município } j

E_{j,\text{total}} = E_{j,\text{pública}} + E_{j,\text{privada}}

\text{Proporção pública}_j = \left( \frac{E_{j,\text{pública}}}{E_{j,\text{total}}} \right) \times 100

\text{Proporção privada}_j = \left( \frac{E_{j,\text{privada}}}{E_{j,\text{total}}} \right) \times 100
```

---

### 2. Percentual de Escolas Públicas Municipais com Acesso à Internet

```math
\text{Percentual com internet}_{j,\text{municipal}} = \left( \frac{\sum_{i=1}^{n_j} X_{ij}}{n_j} \right) \times 100
```

- `Xij = 1` se a escola *i* no município *j* possui internet; `0` caso contrário  
- `nj`: número total de escolas públicas municipais no município *j*

---

### 3. Proporção de Escolas com Acessibilidade Física

```math
\text{Acessibilidade}_j = \left( \frac{\sum_{i=1}^{n_j} x_{ij}}{n_j} \right) \times 100
```

- `xij = 1` se a escola *i* no município *j* possui acessibilidade física; `0` caso contrário  
- `nj`: número total de escolas no município *j*

---

### 4. Tipo de Esgotamento Sanitário nas Escolas

```math
\text{Indicador de esgoto}_{j,k} = \left( \frac{\sum_{i=1}^{n_j} E^{(k)}_{ij}}{n_j} \right) \times 100
```

- `E^(k)ij = 1` se a escola *i* no município *j* possui o tipo de esgotamento *k*; `0` caso contrário  
- `k ∈ {rede pública, fossa séptica, fossa comum, inexistente, outros}`  
- `nj`: número total de escolas no município *j*

---
