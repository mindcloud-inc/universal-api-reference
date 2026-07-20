# Delete Secret with Devin

Deletes an existing secret from Devin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/organizations/:org_id/secrets/:secret_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Delete Secret](https://docs.devin.ai/api-reference/v3/secrets/delete-organizations-secrets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `secret_id` | path | `string` | yes | Secret ID prefixed with secret-. |
