### Run CellPhoneDB on the Vento-Tormo 2018 data

***
##### Login 

1. Login to HPC via ssh

2. Allocate the resource

```
srun --pty -p interactive --mem=8g bash
```

3. Load the modules

```
module load Python
module load R
```
4. Create a working directory

```
cd project
mkdir scRNA-seq-lab3 && cd scRNA-seq-lab3
```

***
##### Install CellPhoneDB

5. Create a python virtual environment 

```
python -m venv cpdb
```

6. Activate the python virtual environment

```
source cpdb/bin/activate
```

7. Install CellPhonedb

```
pip install cellphonedb --use-feature=2020-resolver

pip install markupsafe==2.0.1 --use-feature=2020-resolver
```

***
##### Run CellPhoneDB

8. Run statistical analysis

```
cellphonedb method statistical_analysis --subsampling --subsampling-log false --counts-data gene_name /gpfs/ysm/project/beng469/beng469_jy568/scRNA-seq3/cellphoneDB/data/cell_annotations.txt /gpfs/ysm/project/beng469/beng469_jy568/scRNA-seq3/cellphoneDB/data/log_norm_data_sub.txt
```

9. Plotting

```
cellphonedb 
```
