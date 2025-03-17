# ANMI019 fibre unite

Mapping of shotgun sequencing data against the 2025 version of the UNITE database.

# Usage

## Clone repository

```sh
git clone https://github.com/alberdilab/ANMI019_fibre_unite.git
```

## Add reads and UNITE

Place all reads in: **resources/reads**

```sh
cd ANMI019_fibre_unite/resources/reads
sh getreads.sh
cd ../..
```

Place the decompressed fasta file of the UNITE database (10.15156/BIO/3301232) in: **resources/database**

```sh
cd ANMI019_fibre_unite/resources/database
wget https://s3.hpc.ut.ee/plutof-public/original/b02db549-5f04-43fc-afb6-02888b594d10.tgz
tar zxvf b02db549-5f04-43fc-afb6-02888b594d10.tgz
cd ../..
```

## Run the pipeline

```sh
screen -S ANMI019_fibre_unite
cd ANMI019_fibre_unite
snakemake --workflow-profile profile/slurm
```
