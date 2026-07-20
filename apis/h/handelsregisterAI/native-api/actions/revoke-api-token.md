# Revoke API Token with Handelsregister AI

Revokes an existing API token from Handelsregister AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/auth/tokens/:id`
- **Base URL:** `https://handelsregister.ai/api/v1`
- **Official documentation:** [Revoke API Token](https://handelsregister.ai/en/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the API token to revoke. |
