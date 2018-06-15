# ECB Biological rhythms &  timing of protein-protein interactions Project

---
title: ECB Biological rhythms &  timing of protein-protein interactions Project
author: 
date: 2018-06-15
output:
  prettydoc::html_pretty:
    theme: hpstr
    toc: yes
  pdf_document:
    number_sections: yes
    toc: yes
fontsize: 18pt

---
# Repository Layout

**Data/:**

2018-06-15_ECB_master_data_sheet.xlsx : master datasheet with the collected data; metadata below

**Documents/:**

2018-06-12_ECB_workflow.Rmd: overall workflow


# Setup
* 5 Cohorts:
  * 10 female UZ individuals - 5 RT & 5 SO
  * 10 female BE individuals - 5 RT & 5 SO
  * 10 male UZ individuals - 5 RT & 5 SO
  * 10 male BE individuals - 5 RT & 5 SO

# Overall Workflow

![ECB Workflow](https://github.com/HannahHChu/Notebooks/blob/master/Images/ECBworkflow.png)

```{r}
mermaid("
  graph TD
  A[Cohort Day] --separate eggs--> B[SO diapause]
  A --separate eggs--> C[RT direct development]
  B --5 females UZ & BE and 5 males UZ & BE--> D[46 days, 23ºC, 12L:12D until pupation]
  C --5 females UZ & BE and 5 males UZ & BE--> E[46 days, 23ºC, 16L:8D]
  E --transfer--> F[Diapause termination: 26ºC, 16L:8D until pupation]
  F --eclosion--> G[move adults to Trikinetics in Free Run conditions]
  D --> E")
```
# Meta Data for 2018-06-15_ECB_master_data_sheet.xlsx 

* cohort_date: date that the eggs were laid
* cohort: the cohort number
* individual: individual number assigned by cohort
* strain: UZ or BE (univoltine, bivoltine respectively)
* treatment: SD (simulated diapause) or RT (favorable conditions)
* sex: male or female
* pupation_date: date the insect starts to pupate
* eclosion_date: date the insects eclose
* trik_monitor: TRIK monitor number
* trik_pos: TRIK position within the monitor
* trik_enter_date: date adult enters TRIK
* trik_exit_date: date adult is removed from TRIK and into free run
* fr_trik_monitor: free run TRIK monitor number
* fr_trik_pos: free run TRIK position within the monitor
* fr_trik_enter_date: free run date adult enters TRIK
* fr_trik_exit_date: free run date when adult is removed
* adult_death_date: date adult insect dies


# Session Info
```{r}
sessionInfo()
```