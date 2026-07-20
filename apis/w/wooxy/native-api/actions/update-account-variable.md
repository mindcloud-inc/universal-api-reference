# Update Account Variable with Wooxy

Updates an existing account variable in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/global-variables/update`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Update Account Variable](https://wooxy.com/api-documentation/variables/update-account-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Variable name in lowerCamelCase format. |
| `value` | body | `string` | yes | Updated variable value as a string. |
