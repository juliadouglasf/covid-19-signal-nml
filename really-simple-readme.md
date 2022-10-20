## Setup:

### 0. Clone the git repository

        git clone --recursive https://github.com/phac-nml/covid-19-signal-nml.git

### 1. Install `conda` and `snakemake` 

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh # follow instructions
        source $(conda info --base)/etc/profile.d/conda.sh
        conda create -n signal -c conda-forge -c bioconda -c defaults snakemake pandas conda
        conda activate signal

### 2. Install `mamba`

        conda install -c conda-forge mamba
        mamba create -c conda-forge -c bioconda -n signal snakemake pandas conda
        conda activate signal
