# WGCNA-project_04.07.2024

# WGCNA  — PBS vs LPS (1x / 4x)  snapshot

This repository is a **snapshot** of a WGCNA analysis I ran  with three groups:
- PBS  
- LPS (1x)  
- LPS (4x)

---

## Study design
Total samples: **25**
- PBS: **9**
- LPS (1x): **9**
- LPS (4x): **7**

---

## Key analysis settings 
- Low-expression filter: `meanFPKM = 0`
- Outlier cut height: `hlevel = 40000`
- Soft-threshold search: `powers = 1:15`, target scale-free fit line at `R^2 = 0.90`
- Module detection:
  - `deepSplit = 2`
  - `pamRespectsDendro = FALSE`
  - `minModuleSize = 50`
- Module merging cut height: `MEDissThres = 0.9`
- Cytoscape export:
  - weighted TOM edges
  - `threshold = 0.02`
---


## Output files generated

### A) Filtered expression matrix
- `rt_filter.xls`  
  Filtered expression matrix exported after QC + low-expression filtering  
  (format: sample as first column, genes as subsequent columns).

---

### B) Sample QC / clustering
- `1_samplenet.pdf`  
- `1_samplenet_cut.pdf`  
- `2_sample_map.pdf`  
---

### C) Soft-threshold selection
- `3_independence.pdf`  
---

### D) Network construction and module detection
- `4_gene.pdf`  
- `5_Tree.pdf`  
- `6_module.pdf`  
- `6_module_cut.pdf`  
---

### E) Module–trait association
- `8_Module.pdf`  
---

### F) Gene/module membership tables
- `all_genes.txt`  
- `module_<COLOR>.txt`  
- `GS_MM.xls`  
---

### G) Network heatmaps (TOM-based)
- `10_allgenemap.pdf`  
- `11_selectgenemap.pdf`  
---

### H) Eigengene network plots
- `12_dendrogram.pdf`  
- `13_modulemap.pdf`  
- `14_dendrogrammap.pdf`  
---

### I) Cytoscape exports
- `CytoscapeInput-edges-<COLOR>.txt`
- `CytoscapeInput-nodes-<COLOR>.txt`
---

### J) Expression extraction for selected modules
- `GenesExp.xls`  
---
