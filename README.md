# GET_CONCENSUS (AMPLICONES)

Run pipeline via [nextflow](https://www.nextflow.io/). Notes on building and pushing Docker image are [here](https://hub.docker.com/layers/vici0uz/iics/latest/images/sha256-1c11f1fa0b9a1d3f5cb9a7f7e9e6eb97dfc23b00ea3b3fd3e44ff6bd00c8b068?context=repo)

## REQUIREMENTS
- nextflow
- docker


## SETUP
data in data/input containing
- barcodes
- your_samplesheet.tsv
- your_reference.fasta
- a config.json file with the following structure

```
{
	"sample": "your_samplesheet.tsv",
    "reference": "your_reference.fasta"
}
```
Execute on linux or wsl terminal
```
git clone 'https://github.com/vici0uz/seq_iics'
cd seq_iics
mkdir -p data/input
# copy your data to project data/input directory
nextflow run main.nf --data {myDataDir} --with-docker vici0uz/iics:latest
```

