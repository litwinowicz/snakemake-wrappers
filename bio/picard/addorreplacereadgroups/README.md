# Wrapper for samtools index.

## Example:

```
rule replace_rg:
    input:
        "mapped/{sample}.bam"
    output:
        "fixed-rg/{sample}.bam"
    params:
        "RGLB=lib1 RGPL=illumina RGPU={sample} RGSM={sample}"
    wrapper:
        "0.4.0/bio/picard/addorreplacereadgroups"
```