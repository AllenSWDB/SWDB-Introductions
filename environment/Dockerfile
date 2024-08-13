# hash:sha256:cc09c2eccc2b5e2b45f335aa3926da4bd39007a7c9fcfcc21e4928e231bb7c1e
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.6.1-miniconda4.12.0-python3.9-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive
ARG API_KEY
ARG API_SECRET

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y \
        ipykernel==6.21.3 \
        ipython==8.11.0 \
        ipywidgets==8.1.2 \
        jupyter==1.0.0 \
        jupyterlab==3.6.1 \
        matplotlib-inline==0.1.6 \
        nbclient==0.7.2 \
        nbconvert==7.2.9 \
        nbformat==5.7.3 \
        notebook==6.5.3 \
        pip==24.0 \
        scikit-learn==1.4.2 \
    && conda clean -ya

RUN pip3 install -U --no-cache-dir \
    allensdk==2.16.2 \
    brain-observatory-utilities==0.3.1 \
    brainglobe-atlasapi==2.0.6 \
    brainglobe-space==1.0.2 \
    caveclient==5.22.0 \
    cloud-volume==10.0.0 \
    h5py==3.11.0 \
    hdmf==3.14.1 \
    imageio==2.34.2 \
    imageio-ffmpeg==0.5.1 \
    imageryclient==1.0.4 \
    jax==0.4.30 \
    jaxlib==0.4.30 \
    jupyterlab-myst==2.4.2 \
    jupytext==1.16.2 \
    k3d==2.16.1 \
    matplotlib==3.9.0 \
    meshparty==1.16.14 \
    myst-nb==1.1.1 \
    myst-parser==2.0.0 \
    neuroglancer==2.39.2 \
    nglui==3.3.1 \
    numpy==1.23.5 \
    pandas==1.5.3 \
    pynwb==2.8.0 \
    scipy==1.10.1 \
    seaborn==0.13.2 \
    skeleton-plot==0.0.10 \
    standard-transform==1.4.0 \
    statsmodels==0.14.2 \
    trimesh==4.4.3 \
    umap-learn==0.5.6 \
    xarray==2023.1.0
