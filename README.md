# CoriellIndex_VCF_180306
CoriellIndex vcf files - Analysis options for Next Generation Whole Genome Sequencing

According to the literature search, WGS is currently applied in medical genetics and heritable monogenic disorders, which interrogate germ line variants. Studies reported in the previous paragraph usually conduct variant calling following gold standard GATK pipeline (https://software.broadinstitute.org/gatk/best-practices/), additionally supported in cancer studies by somatic variant callers [do Valle and others 2016]. From technical point of view, the critical step in such pipeline is variant calling, which must be precise, adequate to WGS coverage and to the type of experiment. Our literature search indicates that the most accurate variant calls for 30x human WGS were recently reported by PrecisionFDA Truth Challenge (https://precision.fda.gov/challenges/truth/results). F-score values (Harmonic mean of recall and precision) reached 99.9587% for single nucleotide variants (SNV) and 99.4009% for short indels. DeepVariant tool [Poplin et al., biorxiv] which won the challenge is the first variant calling method which uses TensorFlow machine learning. Thus we ask a question if introduction of machine learning to medical genomics could significantly improve variant analysis precision. To test this hypothesis, we compare DeepVariant tool to recently used methods using independent NA12878 sample sequenced in our laboratory. Furthermore, we used the newest GRCh38.p10 reference genome [Speir and others 2016] whereas Poplin et al. called variants using GRCh37. Results generated by DeepVariant were compared to GATK 4.0 (gold standard pipeline) and Speedseq (efficient pipeline).

Variant files produced by SpeedSeq 0.1.0:
CoriellIndex_S1_speedseq_GRCh38p10_180109.vcf.gz
CoriellIndex_S1_speedseq_GRCh38p10_180109.vcf.gz.tbi

Variant files produced by DeepVariant 0.4.1:
CoriellIndex_deepvariant_GRCh38p10_output_180112.vcf.gz
CoriellIndex_deepvariant_GRCh38p10_output_180112.vcf.gz.tbi

Variant files produced by GATK 4.0.0.0:
CoriellIndex_gatk_GRCh38p10_GVCF.applyRec.INDEL.g_180207.vcf.gz
CoriellIndex_gatk_GRCh38p10_GVCF.applyRec.INDEL.g_180207.vcf.gz.tbi
CoriellIndex_gatk_GRCh38p10_GVCF.applyRec.SNP.g_180207.vcf.gz
CoriellIndex_gatk_GRCh38p10_GVCF.applyRec.SNP.g_180207.vcf.gz.tbi

Reference variant calls (Platinum Genomes):
NA12878-R8_S1-vcf-38345413__NA12878-Platinum-Genomes-v2016-1-0-hg38-.vcf.gz
NA12878-R8_S1-vcf-38345413__NA12878-Platinum-Genomes-v2016-1-0-hg38-.vcf.gz.tbi

Variant files produced by DeepVariant 0.4.1 and filtered for coding exons (Gencode v27):
CoriellIndex_deepvariant_GRCh38p10_output_coding_exons_gencodeV27_180118.vcf.gz
CoriellIndex_deepvariant_GRCh38p10_output_coding_exons_gencodeV27_180118.vcf.gz.tbi

