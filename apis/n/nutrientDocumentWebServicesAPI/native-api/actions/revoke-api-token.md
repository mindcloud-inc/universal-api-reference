# Revoke API Token with Nutrient Document Web Services

Deletes an API token from Nutrient Document Web Services API.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tokens`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Revoke API Token](https://www.nutrient.io/api/reference/public/#tag/JWT/operation/revoke-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Token identifier to revoke. |
