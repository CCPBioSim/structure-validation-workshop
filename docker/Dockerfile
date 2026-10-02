# Start with BioSim base image.
ARG BASE_IMAGE=latest@sha256:9396d59c0b195cb365875343f26a67ef27a6a6260d32be3fcb29323f8bb0ca05
FROM ghcr.io/ccpbiosim/jupyterhub-base:$BASE_IMAGE

LABEL maintainer="James Gebbie-Rayet <james.gebbie@stfc.ac.uk>"

# Switch to jovyan user.
USER $NB_USER
WORKDIR $HOME

# Install workshop deps
RUN pip install --no-cache-dir \
    requests==2.34.2

COPY --chown=1000:100 . .
RUN rm -rf LICENSE README.md docker .git .github

# Copy lab workspace
COPY --chown=1000:100 docker/default-37a8.jupyterlab-workspace /home/jovyan/.jupyter/lab/workspaces/default-37a8.jupyterlab-workspace

# Always finish with non-root user as a precaution.
USER $NB_USER
