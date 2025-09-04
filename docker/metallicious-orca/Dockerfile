FROM continuumio/miniconda3:24.11.1-0

# Based loosely on https://github.com/duartegroup/metallicious?tab=readme-ov-file#installation

# Install orca
# IMPORTANT: we can't publish orca anywhere, so this needs to be run locally after downloading
# the orca installer file from the official route, and the image generated must not be pushed
# to any public repo
COPY orca_6_1_0_linux_x86-64_shared_openmpi418.run orca_6_1_0_linux_x86-64_shared_openmpi418.run
RUN ./orca_6_1_0_linux_x86-64_shared_openmpi418.run

# Install metallicious and dependencies
# psiresp is needed when using orca, and relies on h5py which has no version that works with python >3.9
RUN conda create -n py39 python=3.9
RUN conda activate py39
RUN conda install rdkit autode mdanalysis=2.7.0 networkx numpy==1.26.2 qcelemental==0.25.1 ambertools --channel conda-forge
RUN conda install h5py==3.1.0 --channel conda-forge
RUN conda install psiresp --channel conda-forge
RUN pip install metallicious

