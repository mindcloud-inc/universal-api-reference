# Validate Single Phone MNP Input with Verificaremails

Retrieves a phone MNP validation result from Verificaremails.

## Endpoint

- **Method:** `GET`
- **Path:** `/phonemnp/validate/single`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Validate Single Phone MNP Input](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Phone number with international prefix for MNP lookup. Example: 34934511100. |
