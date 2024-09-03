# hash:sha256:fb06af4377f9b8e4c135832ca54a00d05859353dfcab73dd31d35d9f11f87e13
ARG REGISTRY_HOST
FROM $REGISTRY_HOST/codeocean/lightning-jupyterlab:2.3

ARG DEBIAN_FRONTEND=noninteractive

ARG GIT_ASKPASS
ARG GIT_ACCESS_TOKEN
COPY git-askpass /

RUN apt-get update && apt-get install libgl1 libgtk2.0-dev -y

RUN pip install -U --no-cache-dir \
    git+https://github.com/facebookresearch/segment-anything-2.git \
    matplotlib \
    zarr \
    nibabel \
    pynrrd \
    SimpleITK \
    scipy \
    scikit-image \
    imageio \
    pillow \
    opencv-python \
    natsort \
    albumentations \
    torchmetrics \
    monai[nibabel,skimage] \
    patchify \
    git+https://github.com/huggingface/transformers.git \
    git+https://github.com/facebookresearch/segment-anything.git \
    accelerate
