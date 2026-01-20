
# Tech Challenge Fase 1 – Classificação de câncer de mama com Machine Learning (Regressão Logística)

## Executar com Docker

## Build e execução (Docker)

```bash
  docker build -t tech-challenge-fase1 .
  docker run --rm -it -p 8888:8888 tech-challenge-fase1
```

Abra no navegador: `http://localhost:8888`

## Build e execução (Docker Compose)

```bash
  docker compose up --build
```

> O `docker-compose.yml` monta o diretório local no container (`volumes`), então qualquer alteração no notebook aparece imediatamente.

## Segurança rápida
Por padrão o Dockerfile desativa token/senha do Jupyter (prático para rede local). Se quiser habilitar token:

```bash
  docker run --rm -it -p 8888:8888 \
  -e JUPYTER_TOKEN=meu_token \
  tech-challenge-fase1 \
  jupyter lab --ip=0.0.0.0 --port=8888 --no-browser --allow-root --NotebookApp.token=$JUPYTER_TOKEN
```
