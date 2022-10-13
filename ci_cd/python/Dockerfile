FROM python:3.9-slim
RUN mkdir -p /home/gitlab && addgroup gitlab && useradd -d /home/gitlab -g gitlab gitlab && chown gitlab:gitlab /home/gitlab
RUN apt-get update && apt-get install -y curl
USER gitlab
WORKDIR /home/gitlab
RUN curl -sSL https://install.python-poetry.org | python3 -
ENV PATH=/home/gitlab/.local/bin:$PATH
RUN poetry config virtualenvs.in-project true
