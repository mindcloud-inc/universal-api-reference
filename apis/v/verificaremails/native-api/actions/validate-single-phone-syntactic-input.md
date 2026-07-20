# Validate Single Phone Syntactic Input with Verificaremails

Retrieves a phone syntactic validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/phonesyntactic/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Phone Syntactic Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Phone number with international prefix. Example: 34934511100. |
