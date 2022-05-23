# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.234.0/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version (use ubuntu-22.04 or ubuntu-18.04 on local arm64/Apple Silicon): ubuntu-22.04, ubuntu-20.04, ubuntu-18.04
ARG VARIANT="jammy"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}
# Default packages installed: https://github.com/microsoft/vscode-dev-containers/blob/v0.234.0/containers/ubuntu/.devcontainer/library-scripts/common-debian.sh

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
     && apt-get -y install --no-install-recommends 
# libssl-dev
RUN apt-get -y install build-essential cmake pkg-config ripgrep jq httpie fzf fd-find fasd
RUN rustup target add wasm32-unknown-unknown 
RUN cargo install --locked trunk 
RUN cargo install wasm-bindgen-cli
