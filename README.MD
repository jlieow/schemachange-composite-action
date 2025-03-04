# schemachange

This repo contains an action to run Schemachange described [here](https://github.com/Snowflake-Labs/schemachange)

## Input

```yaml
inputs:
    DRY_RUN:
        description: 'Input "--dry-run" to run in dry run mode.'
        required: false
        default: ""
    SF_DATABASE:
        description: "Snowflake Database."
        required: true
    LOCATION_OF_DDL_SCRIPTS:
        description: "Dir in the repo which contains the DDL scripts."
        required: true
    SF_ACCOUNT:
        description: "Snowflake Account."
        required: true
    SF_USERNAME:
        description: "Snowflake User."
        required: true
    SF_ROLE:
        description: "Snowflake Role."
        required: true
    SF_WAREHOUSE:
        description: "Snowflake Warehouse."
        required: true
    SF_PASSWORD:
        description: "Snowflake User Password."
        required: false
    SF_PRIVATE_KEY:
        description: "Snowflake private key content."
        required: false
    SF_PRIVATE_KEY_FILE_PWD:
        description: "Snowflake private key password."
        required: false
```

## Authentication

The action allows authentication either via `Password` or `Private Key Pair`.

### Password

If you are using `Password` authentication, provide `SF_PASSWORD` and ensure that `SF_PRIVATE_KEY` and `SF_PRIVATE_KEY_FILE_PWD` are not provided as inputs.

### Private Key Pair 

If you are using `Private Key Pair` authentication, provide `SF_PRIVATE_KEY` and `SF_PRIVATE_KEY_FILE_PWD` as inputs.

The private key pair is generated according to the following Snowflake [documentation](https://docs.snowflake.com/en/user-guide/key-pair-auth)
