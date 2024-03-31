ARG SUPERSET_VERSION=3.0.0-py310

FROM apache/superset:${SUPERSET_VERSION}

USER root

RUN pip install --no-cache-dir elasticsearch-dbapi

USER superset

ENV PYTHONUNBUFFERED=1 \
    # prevents python creating .pyc files
    PYTHONDONTWRITEBYTECODE=1 \
    # pip
    PIP_NO_CACHE_DIR=off \
    PIP_DISABLE_PIP_VERSION_CHECK=on \
    PIP_DEFAULT_TIMEOUT=100
