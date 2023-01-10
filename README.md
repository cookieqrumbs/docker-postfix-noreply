# docker-postfix-noreply
[![Docker Image](https://github.com/cookieqrumbs/docker-postfix-noreply/actions/workflows/deploy.yml/badge.svg)](https://github.com/cookieqrumbs/docker-postfix-noreply/actions/workflows/deploy.yml)

A postfix container for sending outbound emails *within internal trusted network*.

## Enable SASL authentication (PLAIN / LOGIN)
Optional Environment variables
- `SMTP_USER` (Default value: **noreply**)

- `SMTP_PASSWORD` (Default value: a random string generated during startup and printed to stdout)

- `SMTP_PASSWORD_FILE` (a file which contains the **SMTP_PASSWORD**)
  - E.g. /run/secrets/smtp_password


## Disable authentication
Optional Environment variable
- `NO_AUTH` = **Y** (Default value: **N**)

Optional Environment variables
- `TRUST_NETWORK` (Default value: **10.0.0.0/16**)
