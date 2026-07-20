# List Account Variables with Wooxy

Retrieves account variables from your Wooxy account.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/global-variables/find`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [List Account Variables](https://wooxy.com/api-documentation/variables/get-account-variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string<string>` | yes | Account variable name. Wooxy runtime currently requires a non-empty string even though the docs say an empty array should list all variables. |
