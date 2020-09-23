## Introduction
`env-sandbox` lets one run a command with specified environment variables.
It helps to keep the development and test commands as simple and clean as possible.

Consider following project directory
```
.
dev.env
run.sh
```

Content of the file `dev.env`
```
# dev.env
PORT=8000
DATABASE_URL=postgres://@127.0.0.1:5432/awesomedb
```

Content of the file `run.sh`
```
# run.sh
#!/bin/sh
echo $PORT
echo $DATABASE_URL
```

If we run `de ./run.sh` we will get following output in the terminal
```
$ de ./run.sh
8000
postgres://@127.0.0.1:5432/awesomedb
```

## Installation
Issue following command in a terminal to install `env-sandbox`

```
curl -o  /tmp/env-sandbox https://raw.githubusercontent.com/ludbek/env-sandbox/master/install && sh /tmp/env-sandbox
```

## Usage
### Development environment
```
de <cmd>
```

It exports environment variables from `dev.env` and runs a command.
It exports environment variables from `user.env` if available.

### Test environment
```
te <cmd>
```

It exports environment variables from `dev.env` and `test.env`, and runs a command.

### Other environment
```
xe <path-to-env-file> <cmd>
```

It exports environment variables in the given env file and runs a command.
