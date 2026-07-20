# Generate API Token with Nutrient Document Web Services

Creates an API token in Nutrient Document Web Services API.

## Endpoint

- **Method:** `POST`
- **Path:** `/tokens`
- **Base URL:** `https://api.nutrient.io`
- **Official documentation:** [Generate API Token](https://www.nutrient.io/api/reference/public/#tag/JWT/operation/generate-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowedOperations[]` | body | `array<string>` | no | Allowed operations for the token. |
| `allowedOrigins[]` | body | `array<string>` | no | Allowed origins for the token. |
| `expirationTime` | body | `number` | no | Token expiration time in seconds. |
