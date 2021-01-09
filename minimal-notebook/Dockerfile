# Copyright (c) Sho Fujita
# Distributed under the terms of the Modified BSD License.
ARG BASE_CONTAINER=jupyter/minimal-notebook
FROM $BASE_CONTAINER

LABEL maintainer="Sho Fujita <fujitash@makino.co.jp>"

USER root

# Install additional libraries with pip
RUN pip install jupyter-contrib-nbextensions \
    pip install jupyter-nbextensions-configurator \
    jupyter contrib nbextension install \
    jupyter nbextensions_configurator enable

# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
