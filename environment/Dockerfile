# hash:sha256:da72291381e6feef545291c0bfa67977bd60ea055bbfa4b2ec4c7509af90f3d1
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/jupyterlab:3.6.1-miniconda4.12.0-python3.9-ubuntu20.04

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN conda install -y \
        pip==24.0 \
        scikit-learn==1.4.2 \
    && conda clean -ya

RUN pip3 install -U --no-cache-dir \
    setuptools==72.2.0
RUN pip3 install -U --no-cache-dir \
    brain-observatory-utilities==0.3.1 \
    brainglobe-atlasapi==2.0.6 \
    brainglobe-space==1.0.2 \
    caveclient==5.22.0 \
    cloud-volume==10.0.0 \
    h5py==3.11.0 \
    hdmf==3.14.1 \
    hdmf-zarr==0.6.0 \
    imageio==2.34.2 \
    imageio-ffmpeg==0.5.1 \
    imageryclient==1.0.4 \
    ipykernel==6.29.5 \
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
    numpy \
    nwbwidgets==0.11.3 \
    pandas==1.5.3 \
    papermill==2.6.0 \
    pynwb==2.8.0 \
    scipy==1.10.1 \
    seaborn==0.13.2 \
    skeleton-plot==0.0.10 \
    standard-transform==1.4.0 \
    statsmodels==0.14.2 \
    trimesh==4.4.3 \
    umap-learn==0.5.6 \
    xarray==2023.1.0

COPY postInstall /
RUN /postInstall
