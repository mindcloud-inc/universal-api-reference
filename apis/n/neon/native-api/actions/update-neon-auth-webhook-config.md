# Update webhook configuration for Neon Auth with Neon

Updates Neon Auth webhook configuration in Neon.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:project_id/branches/:branch_id/auth/webhooks`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Update webhook configuration for Neon Auth](https://api-docs.neon.tech/reference/updateneonauthwebhookconfig)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `enabled` | body | `boolean` | yes | Neon API parameter enabled |
| `webhook_url` | body | `string` | no | Neon API parameter webhook_url |
| `enabled_events[]` | body | `array<list>` | no | Neon API parameter enabled_events |
| `timeout_seconds` | body | `number` | no | Neon API parameter timeout_seconds |
