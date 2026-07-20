# Validate Single Address Input with Verificaremails

Retrieves an address validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/address/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Address Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Address to validate as a single string. |
