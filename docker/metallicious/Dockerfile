FROM continuumio/miniconda3:24.11.1-0

# Based loosely on https://github.com/duartegroup/metallicious?tab=readme-ov-file#installation
# Versions chosen to work with python 3.12 and fit https://github.com/duartegroup/metallicious/blob/main/requirements.txt

RUN conda install rdkit autode mdanalysis=2.7.0 networkx numpy==1.26.2 qcelemental==0.25.1 ambertools --channel conda-forge

RUN pip install metallicious

