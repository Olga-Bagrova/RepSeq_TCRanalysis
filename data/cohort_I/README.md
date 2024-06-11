## Directory Structure
  - `./data` *Rep-seq data after MIGEC & MiXCR or VDJtools preprocessing for cohort I*
  - `./data_corrected` *corrected gene-usage with using mirpy*
  - `./metadata` *metadata for cohort_I*
  - `./nonfunctional` *data with only non-functional sequences (the CDR3 region contains a stop-codon * or a frameshift _)*
  - `./nonfunctional_corrected` *corrected only non-functional sequences' gene-usage with using mirpy*
  - `./onlyfunctional` *data with only functional sequences (the CDR3 region does not contain a stop-codon * or a frameshift _)*
  - `./onlyfunctional_corrected` *corrected only functional sequences' gene-usage with using mirpy*  

> Be careful! The `./data`, `./nonfunctional`, `./onlyfunctional` directories contain only 1000 samples. To get the full set, please, contact the authors.
