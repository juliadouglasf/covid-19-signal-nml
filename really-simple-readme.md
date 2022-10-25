## Setup:

### 0. Clone the git repository

        git clone --recursive https://github.com/phac-nml/covid-19-signal-nml.git

### 1. Install `conda` and `snakemake` 

        wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
        bash Miniconda3-latest-Linux-x86_64.sh # follow instructions
        source $(conda info --base)/etc/profile.d/conda.sh
        conda create -n signal -c conda-forge -c bioconda -c defaults snakemake pandas conda
        conda activate signal

### 2. Get dependencies

        cd covid-19-signal-nml
        bash scripts/get_data_dependencies.sh -d data -a MN908947.3
        
### 3. Create a directory called 'fastq' within covid-19-signal-nml

        mkdir fastq
        
### 4. Add paired fastq files to the fastq directory

### 5. Run the pipeline

        cd ~/covid-19-signal-nml
        bash run_signal.sh -d ./fastq -p articV3
