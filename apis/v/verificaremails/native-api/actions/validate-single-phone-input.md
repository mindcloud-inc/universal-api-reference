# Validate Single Phone Input with Verificaremails

Retrieves a phone validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Phone Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Phone number to validate with international prefix. Example: 34934511100. |
