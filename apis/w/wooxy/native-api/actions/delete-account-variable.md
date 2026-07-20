# Delete Account Variable with Wooxy

Deletes an existing account variable from Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/global-variables/remove`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Delete Account Variable](https://wooxy.com/api-documentation/variables/remove-account-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Variable name in lowerCamelCase format. |
