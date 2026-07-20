# Validate Single Email Input with Verificaremails

Retrieves an email validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Email Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Email address to validate. Provide a single email string. |
