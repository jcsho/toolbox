FROM registry.fedoraproject.org/f33/fedora-toolbox:33

ARG BUILD_DATE
ARG VERSION
ARG REVISION

# Update labels
LABEL summary="Development container using toolbox. Based on Fedora"
LABEL maintainer="Justin Ho <justinho@jcsh.dev>"
LABEL build-date=$BUILD_DATE
LABEL org.opencontainers.image.created=$BUILD_DATE
LABEL org.opencontainers.image.authors="Justin Ho <justinho@jcsh.dev>"
LABEL org.opencontainers.image.url="https://github.com/jcsho/toolbox"
LABEL org.opencontainers.image.documentation="https://github.com/jcsho/toolbox/blob/master/README.md"
LABEL org.opencontainers.image.source="https://github.com/jcsho/toolbox"
LABEL org.opencontainers.image.version=$VERSION
LABEL org.opencontainers.image.revision=$REVISION
LABEL org.opencontainers.image.vendor="Justin Ho <justinho@jcsh.dev>"
LABEL org.opencontainers.image.licenses="MIT"
LABEL org.opencontainers.image.title="Fedora Base"
LABEL org.opencontainers.image.description="Development container using toolbox. Based on Fedora"

# Base applications
RUN dnf -yq install zsh fd-find ripgrep neovim bat pinentry python3-neovim git-delta tmux

# Temporary fix for missing locale
# https://github.com/containers/toolbox/issues/60
RUN dnf -yq swap glibc-minimal-langpack glibc-langpack-en
