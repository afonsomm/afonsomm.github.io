FROM afonsomm/micromamba-quarto-dev:latest

RUN apt update && apt install default-jdk

USER $MAMBA_USER

# https://telatin.github.io/microbiome-bioinformatics/Micromamba/
COPY --chown=$MAMBA_USER:$MAMBA_USER environment.yaml /tmp/env.yaml

ARG MAMBA_DOCKERFILE_ACTIVATE=1

RUN micromamba install -y --file env.yaml && \
     micromamba clean --all --yes