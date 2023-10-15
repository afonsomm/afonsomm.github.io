FROM mambaorg/micromamba:latest

USER root

RUN apt update && apt install git

ADD https://github.com/quarto-dev/quarto-cli/releases/download/v1.3.450/quarto-1.3.450-linux-amd64.deb ./quarto.deb

RUN apt-get install ./quarto.deb

USER $MAMBA_USER