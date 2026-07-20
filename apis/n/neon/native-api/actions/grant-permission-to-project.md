# Grant project access with Neon

Grants project access in Neon.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/permissions`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Grant project access](https://api-docs.neon.tech/reference/grantpermissiontoproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `email` | body | `string` | yes | Neon API parameter email |
