FROM mcr.microsoft.com/devcontainers/python:1-3.12-bullseye

# Update pip
RUN pip install --upgrade pip

#Install poetry official way
USER vscode
RUN curl -sSL https://install.python-poetry.org | python -
ENV PATH = "${PATH}:/home/vscode/.local/bin"

## Git setup
RUN git config --global diff.tool vscode && git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'