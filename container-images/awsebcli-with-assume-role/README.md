# awsebcli-with-assume-role

[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/sgreben/awsebcli-with-assume-role.svg)](https://hub.docker.com/r/sgreben/awsebcli-with-assume-role/builds) [![Docker Repository on Quay](https://quay.io/repository/sgreben/awsebcli-with-assume-role/status "Docker Repository on Quay")](https://quay.io/repository/sgreben/awsebcli-with-assume-role) [![pipeline status](https://gitlab.com/sgreben/docker-awsebcli-with-assume-role/badges/master/pipeline.svg)](https://gitlab.com/sgreben/docker-awsebcli-with-assume-role/pipelines)

Provides a wrapper `with-assume-role` to run commands under an assumed role (defined by the value of the environment variable `ASSUME_ROLE_ARN`).

Latest releases of `awsebcli` are automatically tracked, updated in [./requirements.txt](requirements.txt), and built as tagged Docker images (e.g. `sgreben/awsebcli-with-assume-role:3.15.2`) using [Renovate](https://renovatebot.com), [Gitlab CI](https://gitlab.com/sgreben/docker-awsebcli-with-assume-role/pipelines), and [Quay.io](https://quay.io/repository/sgreben/awsebcli-with-assume-role?tab=builds)/[DockerHub](https://hub.docker.com/r/sgreben/awsebcli-with-assume-role/builds).

## Usage

```
docker build -t kreebo/awsebcli-with-assume-role
```

```
export ASSUME_ROLE_ARN=arn:aws:iam::123456789012:role/demo
export AWS_PROFILE=<your_sso_profile>

```
docker compose build
```

then,

```
docker compose up
```

you can then exec into the container terminal using

```
docker exec -it awsebcli-with-assume-role-ebcli-1 sh
```
