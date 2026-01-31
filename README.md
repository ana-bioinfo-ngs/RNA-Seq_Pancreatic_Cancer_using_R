# RNA-Seq on Pancreatic Cancer Dataset

DATASET NAME: MiR-802 is a Tumor Suppressor of Early Stage Pancreatic Cancer

This study aims to investigate the transcriptional changes associated with miR-802 activity using RNA-seq count data obtained from Expression Atlas. By identifying differentially expressed genes and enriched biological pathways, we seek to understand the molecular mechanisms underlying miR-802–mediated tumor suppression.

Objectives: 

1. To analyze RNA-seq count data from early-stage pancreatic cancer samples
2. To identify significantly upregulated and downregulated genes
3. To visualize global expression patterns using clustering and volcano plots
4. To perform functional enrichment analysis (GO and KEGG)

RNA-seq raw count data were obtained from the EMBL-EBI Expression Atlas database. The dataset consists of mouse (Mus musculus) pancreatic tissue samples collected from an established genetically engineered mouse model of pancreatic neoplasia. All samples were derived from adult mice aged 10–12 weeks. The experimental design includes two genetically defined groups, both of which carry the pancreatic cancer–predisposing background - (1) Control (Reference) samples: samples represent pancreatic neoplastic tissue in the presence of normal miR-802 activity. (2) Test samples: These samples represent pancreatic neoplastic tissue with  miR-802 expression absent.
Each group consists of four independent biological replicates (total of eight samples), with each sample corresponding to a distinct individual mouse.

## Methodology
1. Data Preprocessing

Raw count matrix and sample metadata were imported into R
Sample metadata was aligned with count matrix columns



Lowly expressed genes were filtered to reduce noise


