## Introduction
`env-sandbox` lets one run same command in different environments.
It helps to keep the development and test commands as simple and clean as possible.

## Usage
### Development environment

```
devenv <cmd>
```

It runs a command inside development environment.
It exports environment variables from `dev.env` before running a command.
It exports environment variables from `user.env` if available.

### Test environment

```
testenv <cmd>
```

It runs a command inside test environment.
It exports environment variables from `dev.env` and `test.env` before running a command.
It exports environment variables from `user.env` if available.
