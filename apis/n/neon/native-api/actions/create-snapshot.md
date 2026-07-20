# Create snapshot with Neon

Creates a snapshot in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/branches/:branch_id/snapshot`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Create snapshot](https://api-docs.neon.tech/reference/createsnapshot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `branch_id` | path | `string` | yes | Neon API parameter branch_id |
| `lsn` | query | `string` | no | Neon API parameter lsn |
| `timestamp` | query | `string` | no | Neon API parameter timestamp |
| `name` | query | `string` | no | Neon API parameter name |
| `expires_at` | query | `string` | no | Neon API parameter expires_at |
