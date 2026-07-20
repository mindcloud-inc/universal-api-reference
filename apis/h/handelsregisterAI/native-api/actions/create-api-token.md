# Create API Token with Handelsregister AI

Creates a new API token in Handelsregister AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/tokens/create`
- **Base URL:** `https://handelsregister.ai/api/v1`
- **Official documentation:** [Create API Token](https://handelsregister.ai/en/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token_name` | body | `string` | yes | Name for the API token to create. |
| `expires_at` | body | `string` | no | Optional token expiration timestamp. |
