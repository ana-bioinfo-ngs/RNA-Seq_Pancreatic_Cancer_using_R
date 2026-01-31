# RNA-Seq on Pancreatic Cancer Dataset

DATASET NAME: [MiR-802 is a Tumor Suppressor of Early Stage Pancreatic Cancer](https://www.ebi.ac.uk/gxa/experiments/E-MTAB-10411/Experiment%20Design)

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

- Raw count matrix and sample metadata were imported into R
- Sample metadata was aligned with count matrix columns

<img width="590" height="678" alt="IMG1" src="https://github.com/user-attachments/assets/87940251-643f-4959-b74e-8464725785c0" /> <br/><br/>

- Lowly expressed genes were filtered to reduce noise

<img width="837" height="662" alt="IMG2" src="https://github.com/user-attachments/assets/982d09a1-5dba-45e4-9c88-ff2e02a6257d" /> <br/><br/><br/>

2. Normalization using DESeq2

Normalization was performed using the DESeq2 package to account for sequencing depth and size factor estimation to get normalized counts.

<img width="392" height="682" alt="IMG3" src="https://github.com/user-attachments/assets/be033b99-7950-42d8-b47c-6ed9db4e8ced" /> <br/><br/><br/>


3. Differential Expression Testing

- Run the Differential Expression Analysis using DESeq function on dds.

<img width="407" height="775" alt="IMG4" src="https://github.com/user-attachments/assets/a6359c20-88cc-4f4d-af7d-b29fa27b202e" /> <br/><br/>

- Filter Upregulated and Downregulated genes

<img width="323" height="370" alt="IMG5" src="https://github.com/user-attachments/assets/f2097155-15ee-4e01-87c1-ccd2b5381833" /> <br/><br/><br/>

4. Gene Classification

<img width="372" height="600" alt="IMG6" src="https://github.com/user-attachments/assets/b8f6a38a-9719-405c-865b-cdeb70217b97" /> <br/><br/><br/>

5. Visualization

- Volcano Plot

Filter the top 5 significant upregulated and downregulated genes on the basis of padj values

<img width="422" height="697" alt="IMG7" src="https://github.com/user-attachments/assets/e225e030-9f21-4b22-99f2-60ba717ef4ac" />

<img width="742" height="576" alt="IMG8 - volcano plot" src="https://github.com/user-attachments/assets/3202fc2a-2268-4689-a5a9-db75195c4e60" /> <br/><br/>

- Heatmap

Select the top 50 differentially expressed genes.
Use sample metadata to color samples by condition (Reference and Test).

<img width="418" height="388" alt="IMG9" src="https://github.com/user-attachments/assets/dececcc4-3d60-42c0-b7af-f585cfe1338e" />

<img width="670" height="625" alt="IMG10 - Heatmap" src="https://github.com/user-attachments/assets/921a28c2-87ad-4f63-a784-a3d108d4aceb" /> <br/><br/><br/>


6. Functional Enrichment

Convert mouse Ensembl gene IDs into Entrez gene IDs.using bitr() function for both upregulated and downregulated genes.

<img width="683" height="768" alt="IMG11" src="https://github.com/user-attachments/assets/f959e975-3fb3-4523-9491-24f670513bf3" /> <br/><br/>

- Find biological processes enriched among upregulated and downregulated genes using enrichGO(...)
- Find KEGG pathways that are significantly enriched among upregulated and downregulated genes using enrichKEGG()
- Convert the result data into csv files for upregulated and downregulated genes.

<img width="415" height="580" alt="IMG12" src="https://github.com/user-attachments/assets/8e511874-aced-42fe-868d-b2e34a2ad40c" /> <br/><br/><br/>


7. Conclusion

This RNA-seq analysis identified significant transcriptional and pathway-level changes associated with miR-802 in early-stage pancreatic cancer. The results can be analyzed further to determine a tumor suppressor role for miR-802.









