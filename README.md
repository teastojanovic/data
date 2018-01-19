# Data description


## BreastCancerAll.original.arff

- Each row corresponds to a subject (person), for which a number of DNA measurements have been recorded and breast cancer classification type has been determined.
- Variable names for DNA measurements have the following format:
    - Examples:
        - `1_chrom1_reg2927-43870_probloss`
        - `2_chrom1_reg2927-43870_probnorm`
        - `3_chrom1_reg2927-43870_probgain`
        - `4_chrom1_reg2927-43870_call`
    - Name format: `<id_nr>_chrom<chrom_nr>_reg<region_start>_<region_end>_{probloss|probnorm|probgain|call}`
        - Where `id_nr` is unique identifier for variable,
        - `chrom_nr` is chromosome number,
        - `region_start` and `region_end` denote start and end locations on the chromosome,
        - `probloss`, `probnorm`, `probgain` are probabilities used to determine the call classification for respective region on the chromosome,
        - call is a measure for chromosomal abnormality (+1 for net gain, -1 for loss and 0 for normal amount of genetic material).
- `class`: Breast cancer classification type (HR+, HER2+ or TN)


## BreastCancerAll.reduced.using.cfs.arff

- Obtained from `BreastCancerAll.original.arff` using Correlation Feature Selection (CFS).
- Contains a subset of features of `BreastCancerAll.original.arff`. See above for data description.
