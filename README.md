# Hooma - ERP - Backend Monorepo
___

# 🏍️ Rush
This monorepo is based on rush, some rules applies

## Warnings
___

- *DO NOT USE CUSTOM SCRIPTS*
- *DO NOT CREATE CUSTOM CONFIGS*

## Installation
___

### Prerequisites

- node.js
- rush

```shell
npm install -g @microsoft/rush
```

### SSL certificates
Since we are using http2 protocol, we need to use SSL connections even on local. So we are using self signed certificates
```shell
make cert_gen
```

## Dependencies installation
*Avoid using package managers command to install / update packages, use instead rush command*

# 🧱 Contributions
___

## Commits
We are using Git hooks. Make sure your commits respects those rules:

- conventional commits

# Development guidelines

- make you code agnostic
- use adapters to link dependencies (DB, etc.)
- the example service is authentifier
  - Please refer to it before any structural decision

## Services

### Configs
Use dedicated make command to sync config


```shell
make sync_ts_config
```




## Ports (for local)

### Authentifier

APACHE=443
NODE=3000 (not mapped)
DB=27017 (not mapped)

### Signifier

APACHE=3000
NODE=3000 (not mapped)
DB=27017 (not mapped)

### Userifier

APACHE=3001
NODE=3000 (not mapped)
DB=27017 (not mapped)
