# From Gene Mutation to Disease: Investigating How DNA Sequence Changes Affect Protein Products and Human Phenotypes

# Disease Background

Factor V Leiden thrombophilia is an inherited blood-clotting disorder caused by resistance of factor V to inactivation by activated protein C (APC), which increases the tendency to form abnormal venous blood clots. The major clinical characteristic is an increased risk of venous thromboembolism (VTE), particularly deep vein thrombosis (DVT), usually in the legs, and pulmonary embolism (PE). The condition primarily affects the blood coagulation system and venous circulation rather than a specific organ. Its genetic basis is a germline variant in the F5 gene, most commonly c.1601G>A, which results in the amino-acid substitution p.Arg534Gln, historically called p.Arg506Gln (R506Q). This variant makes factor V relatively resistant to cleavage and inactivation by APC, allowing coagulation activity to persist longer. Factor V Leiden follows an autosomal dominant inheritance pattern with variable penetrance; heterozygous individuals have an increased risk of VTE, while homozygous individuals have a substantially higher risk (Pastori et al., 2024; MedlinePlus Genetics, 2023; NCBI ClinVar, 2026).

# Gene and Normal Protein Function

The official gene symbol is F5, which stands for coagulation factor V, and it is located on chromosome 1 at 1q24.2. The F5 gene encodes coagulation factor V, a large plasma glycoprotein that functions as an essential cofactor in the blood coagulation cascade. Normally, activated factor V (factor Va) combines with factor Xa, calcium, and phospholipid surfaces to form the prothrombinase complex, which converts prothrombin into thrombin. Thrombin then converts fibrinogen into fibrin, leading to the formation of a stable blood clot. Factor V is produced primarily by liver cells and secreted into the blood plasma, where it circulates in an inactive form; therefore, its main functional location is extracellularly in the bloodstream. It participates mainly in the common pathway of the blood coagulation cascade and is also involved in the regulatory pathway controlled by activated protein C (APC), which normally inactivates factor V to prevent excessive coagulation.

# Documented Mutation

| Gene | F5 |
|---|---|
| Reference transcript | NM_000130.4 (F5) |
| Exact variant notation | NM_000130.4(F5):c.1601G>A (p.Arg534Gln) |
| Nucleotide change | c.1601G>A |
| Predicted protein change | p.Arg534Gln (R534Q) |
| Mutation type | Missense single-nucleotide variant (SNV) |
| ClinVar accession | VCV000000642.133; Variation ID 642 |
| Clinical interpretation | Pathogenic; associated with activated protein C resistance and an increased risk of venous thrombosis (Factor V Leiden thrombophilia). |
| Scientific references supporting the association | Bertina et al. (1994), PMID: 8164741; Voorberg et al. (1994), PMID: 7910348; Rosendaal et al. (1995); Ridker et al. (1995). |

# Hypothesis

It is hypothesized that the `c.1601G>A` substitution in the *F5* gene changes the encoded amino acid at position 534 from arginine to glutamine (`p.Arg534Gln`). Since this residue is located within an important region involved in Factor V regulation by activated protein C (APC), the substitution may alter the normal cleavage and inactivation of Factor V. Although the mutation is not expected to change the reading frame or overall protein length, the altered amino acid may affect Factor V activity, resulting in prolonged coagulation activity and an increased tendency for venous clot formation.

# Methods

The *F5* gene sequence was analyzed computationally to determine how the selected nucleotide changes could affect the resulting Factor V protein.

1. **Reference Sequence Preparation:** The wild-type *F5* coding and protein sequences were obtained from the NCBI database and used as the reference for all subsequent analyses.

2. **Mutation Construction:** Two mutant sequences were prepared from the wild-type coding sequence. The documented `c.1601G>A` variant was used to represent the known Factor V Leiden mutation, while a separate `G>A` substitution at nucleotide position 10 was created as the artificial mutation.

3. **Protein Prediction:** The wild-type and modified coding sequences were translated with EMBOSS Transeq using Reading Frame 1. The resulting protein sequences were examined for changes in amino acid composition, premature termination, and protein length.

4. **Sequence Alignment:** The translated wild-type and documented mutant were compiled into one FASTA file and analyzed using Needle tool. The alignment was used to identify the exact amino acid positions affected by each nucleotide substitution and to determine whether additional sequence changes occurred.

5. **Result Interpretation:** The observed sequence differences were compared with the expected effects of each mutation to determine whether the substitutions were synonymous or missense and whether they produced changes in the reading frame or protein length.

6. **Data Organization:** The sequences, alignment results, and analysis outputs were organized in Galaxy and documented in the GitHub repository to maintain a clear record of the computational workflow.

# Results

| Parameter | Transeq Result | NCBI Reference (NP_000121.2) |
|---|---|---|
| CDS length | 6,675 bp | 6,675 bp |
| Protein length | 2,225 amino acids | 2,225 amino acids |
| Start codon | ATG | ATG |
| Stop codon | TAG | TAG |
| Reading frame | +1 | +1 |
| First 10 amino acids | MFPGCPRLWV | MFPGCPRLWV |
| Last 10 amino acids | RLELFGCDIY | RLELFGCDIY |

# WT versus Mutant Protein Comparison

The wild-type and mutant Factor V protein sequences were compared to determine the effects of the nucleotide substitution. The documented c.1601G>A mutation resulted in a single amino acid change at position 534, where arginine (R) was replaced by glutamine (Q), producing the substitution p.Arg534Gln (R534Q). The overall protein length remained unchanged, and no insertions, deletions, frameshift, or premature stop codons were observed. This indicates that the mutation is a missense substitution that changes one amino acid while maintaining the rest of the protein sequence.

# Artificial Mutation Experiment

| Parameter | Wild-type | Documented Mutation<br>(c.1601G>A) | Artificial Mutation<br>(c.10G>A) |
|---|---|---|---|
| CDS length | 6,675 bp | 6,675 bp | 6,675 bp |
| Protein length | 2,224 aa | 2,224 aa | 2,224 aa |
| Mutation type | No Mutation | Single-nucleotide substitution (SNV) | Single-nucleotide substitution (SNV) |
| Has the reading frame changed? | No | No | No |
| Premature stop codon appeared? | No | No | No |
| Amino acid was affected | None | Arginine at 534 | Glycine at 4 |
| Expected functional consequence | Normal Factor V sequence | Alters an activated protein C cleavage site, producing activated protein C resistance | May alter the N-terminal region of Factor V, but its specific functional effect cannot be concluded from sequence alone |

# Molecular Interpretation: Gene → Mutation → Protein → Cellular Effect → Phenotype

F5 gene
→ c.1601G>A nucleotide substitution
→ p.Arg534Gln (R534Q) missense change in Factor V
→ Reduced inactivation of Factor V by activated protein C (APC), resulting in prolonged coagulation activity
→ Increased tendency for venous blood clot formation and risk of venous thrombosis (Factor V Leiden)

# Limitations 

This study was limited to in-silico analysis of the *F5* gene and its predicted protein sequence. The computational methods were able to identify nucleotide and amino acid changes, but they could not directly measure the effects of the mutations on Factor V structure, APC cleavage, coagulation activity, or thrombin generation. The functional interpretation of the artificial `c.10G>A` mutation is also limited because its biological effect cannot be confirmed from sequence analysis alone. In addition, sequence alignment and translation results depend on the reference sequence and computational tools used. Therefore, laboratory-based functional assays and experimental studies would be needed to confirm the predicted molecular and physiological effects.

# Conclusion

Based on the results, the wild-type and mutant F5 sequences had the same CDS and protein length, and no changes in the reading frame or premature stop codons were observed. The documented c.1601G>A mutation produced a single amino acid substitution, changing arginine to glutamine at position 534 (p.Arg534Gln). This result is consistent with a missense mutation and with the known Factor V Leiden variant associated with activated protein C resistance. The artificial c.10G>A mutation also resulted in a single amino acid change at the fourth amino acid, but its actual effect on Factor V function cannot be determined from the sequence analysis alone. Overall, the computational results showed that both mutations changed specific amino acids without altering the overall protein length or reading frame.

# Reference

Bertina, R. M., Koeleman, B. P. C., Koster, T., Rosendaal, F. R., Dirven, R. J., de Ronde, H., van der Velden, P. A., & Reitsma, P. H. (1994). Mutation in blood coagulation factor V associated with resistance to activated protein C. Nature, 369(6475), 64–67. https://doi.org/10.1038/369064a0

Greengard, J. S., Sun, X., Xu, X., Fernandez, J. A., Griffin, J. H., & Evatt, B. (1994). Activated protein C resistance caused by Arg506Gln mutation in factor Va. The Lancet, 343(8909), 1361–1362. https://doi.org/10.1016/S0140-6736(94)92497-X

Rosendaal, F. R., Koster, T., Vandenbroucke, J. P., & Reitsma, P. H. (1995). High risk of thrombosis in patients homozygous for factor V Leiden (activated protein C resistance). Blood, 85(6), 1504–1508.

Ridker, P. M., Hennekens, C. H., Lindpaintner, K., Stampfer, M. J., & Miletich, J. P. (1995). Mutation in the gene coding for coagulation factor V and the risk of myocardial infarction, stroke, and venous thrombosis in apparently healthy men. New England Journal of Medicine, 332(14), 912–917. https://doi.org/10.1056/NEJM199504063321403

Pastori, D., Menichelli, D., Valeriani, E., & Pignatelli, P. (2024). Factor V Leiden thrombophilia. In GeneReviews®. University of Washington, Seattle. https://www.ncbi.nlm.nih.gov/books/NBK1368/

MedlinePlus Genetics. (2023). Factor V Leiden thrombophilia. National Library of Medicine. https://medlineplus.gov/genetics/condition/factor-v-leiden-thrombophilia/
