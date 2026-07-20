# Create Account Variable with Wooxy

Creates a new account variable in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/global-variables/create`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Account Variable](https://wooxy.com/api-documentation/variables/create-account-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Variable name in lowerCamelCase format. |
| `value` | body | `string` | yes | Variable value as a string. |
