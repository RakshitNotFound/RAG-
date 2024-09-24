ARG IMAGE=bullseye
FROM mcr.microsoft.com/devcontainers/${IMAGE}

ENV PYTHONUNBUFFERED 1

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive

RUN apt-get -y install --no-install-recommends postgresql-common \
    && /usr/share/postgresql-common/pgdg/apt.postgresql.org.sh -y

RUN apt-get -y install --no-install-recommends postgresql-client-16 \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*