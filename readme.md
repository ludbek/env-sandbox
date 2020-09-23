## Introduction
`env-sandbox` lets one run same command in different environments.
It helps to keep the development and test commands as simple and clean as possible.

Below is an example of the content an environment file.
```
# example content of an environment file

PORT=8000
DATABASE_URL=postgres://@127.0.0.1:5432/awesomedb
```

## Usage
### Development environment
```
de <cmd>
```

It runs a command inside development environment.
It exports environment variables from `dev.env` before running a command.
It exports environment variables from `user.env` if available.

### Test environment
```
te <cmd>
```

It runs a command inside test environment.
It exports environment variables from `dev.env` and `test.env` before running a command.
It exports environment variables from `user.env` if available.

### Other environment
```
xe <path-to-env-file> <cmd>
```

It runs a command inside the environment created by the specified file.
It exports environment variables from the specified file.
