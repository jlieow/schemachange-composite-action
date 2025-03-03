# schemachange

This repo contains a action to run Schemachange described [here](https://github.com/Snowflake-Labs/schemachange)

## Input

```yaml
inputs:
    DRY_RUN:
        description: ""
        required: false
        default: ""
    SF_DATABASE:
        description: ""
        required: true
    LOCATION_OF_DDL_SCRIPTS:
        description: ""
        required: true
    SF_ACCOUNT:
        description: ""
        required: true
    SF_USERNAME:
        description: ""
        required: true
    SF_ROLE:
        description: ""
        required: true
    SF_WAREHOUSE:
        description: ""
        required: true
    SF_PASSWORD:
        description: ""
        required: true
```
