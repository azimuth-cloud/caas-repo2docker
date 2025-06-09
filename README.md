# caas-repo2docker

This repository adapts [repo2docker](https://repo2docker.readthedocs.io) for use within the
Cluster-as-a-Service system of the [Azimuth Cloud Portal](https://github.com/azimuth-cloud/azimuth).

## Developing locally

To run the GitHub Actions linters locally, use:

```sh
docker run --rm \
    -e RUN_LOCAL=true \
    --env-file "super-linter.env" \
    -v "$(pwd)":/tmp/lint \
    ghcr.io/super-linter/super-linter:v7.3.0
```

```sh
ansible-lint -c .ansible-lint.yml
```
