# Get webhook configuration for Neon Auth with Neon

Retrieves Neon Auth webhook configuration from Neon.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/webhooks`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Get webhook configuration for Neon Auth](https://api-docs.neon.tech/reference/getneonauthwebhookconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
