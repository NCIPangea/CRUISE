# Getting Started with CRISPIN

TODO intro paragraph

## Installation

CRISPIN is installed on the Biowulf and FRCE clusters as part of the
`ccbrpipeliner` module.
If you'd like to run the pipeline in a different execution environment,
take a look at [how to run the nextflow pipeline directly](nextflow.md).

## Prepare a sample sheet

TODO

## Initialize

Copy the configuration files to your current working directory

```sh
crispin init
```

## Run

TODO preview, stub, mode=slurm

TODO required params

Run preview to view processes that will run:

```sh
crispin run -profile test -preview
```

Launch a stub run to view processes that will run and download containers:

```sh
crispin run -profile test,singularity -stub
```

Run the test dataset using the test profile:

```sh
crispin run -profile test,singularity
```

or explicitly specify the output directory and input:

```sh
crispin run -profile singularity --outdir results/test --input assets/samplesheet_test.csv
```

### Custom reference genome

TODO different required params

Create and use a custom reference genome:

```sh
crispin run -profile test -entry MAKE_REFERENCE
crispin run -profile test -c results/test/genome/custom_genome.config
```
