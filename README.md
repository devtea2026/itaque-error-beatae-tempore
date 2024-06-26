[![CD Build](https://github.com/devtea2026/itaque-error-beatae-tempore/actions/workflows/cd.yml/badge.svg?branch=main)](https://github.com/devtea2026/itaque-error-beatae-tempore/actions/workflows/cd.yml)

# @devtea2026/itaque-error-beatae-tempore

This JavaScript library aims to fetch access credentials stored in AWS service called AWS Secrets Manager and generate a .env file that contains the necessary environment variables for the development of your application.

### Using

```
    $ npx @devtea2026/itaque-error-beatae-tempore
```

When the library is called using the command above, it reads by default the .env.example file in the current directory, which must contain the following lines:

```env
# service name exactly as defined in AWS Secrets Manager
SVC_NAME=

# Tokens found under "Command line or programmatic access"
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY_ID=
AWS_SESSION_TOKEN=
```

These lines are read to obtain the necessary information to access the AWS Secrets Manager.

If the developer wants the library to read another file, they can pass it as a parameter in the command call, for example:

```
    $ npx @devtea2026/itaque-error-beatae-tempore --envFile .env.test
```

In this case, the library will read the .env.test file instead of the .env.example file.
