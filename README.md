# Example Nextflow MLST pipeline

This pipeline is an example MLST pipeline (using <https://github.com/tseemann/mlst>).

A write-up of this pipeline is at <https://github.com/phac-nml/nf-pipelines/issues/3>.

*Note: This isn't necessarily going to be the final implementation of allele calling. This is just a test pipeline.*

If you have Nextflow and Docker installed, you can test it out with:

```bash
nextflow run apetkau/nf-core-mlstprofiler -profile docker,test -r dev -latest --outdir results
```

Or, if you wish to use your own data:

```bash
nextflow run apetkau/nf-core-mlstprofiler -r dev -latest -profile docker --input samplesheet.csv --outdir results
```

Here, the `samplesheet.csv` lists the sample assemblies or paired reads in a CSV file. An example is below:

**samplesheet.csv**:

| sample  | assembly_fasta | fastq_1      | fastq_2      |
| ------- | -------------- | ------------ | ------------ |
| SampleA | A.fasta        |              |              |
| SampleB |                | B_1.fastq.gz | B_2.fastq.gz |
