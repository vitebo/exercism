# Exercism

## Basic setup

```sh
docker volume create exercism-config

alias exercism='docker run \
  -v "$PWD":/home/exercism \
  -v exercism-config:/root/.config/exercism \
  --rm \
  vitebo/exercism:v1.0.0 \
  exercism \
'

exercism configure --token=$EXERCISM_TOKEN --workspace=/home/exercism
```
