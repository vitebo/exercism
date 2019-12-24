# Exercism

Code practice and mentorship for everyone.

## Image

the image can be found in the [docker hub](https://hub.docker.com/r/vitebo/exercism).

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

after setup, thanks to the alias you can use the CLI normally.

## Customize

To change the desktop, you must update the aliased volume to the desired directory.

**important:** do not change workspace directly inside container.
