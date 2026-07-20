# Revoke project access with Neon

Revokes a project access from Neon.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/permissions/:permission_id`
- **Base URL:** `https://console.neon.tech/api/v2`
- **Official documentation:** [Revoke project access](https://api-docs.neon.tech/reference/revokepermissionfromproject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Neon API parameter project_id |
| `permission_id` | path | `string` | yes | Neon API parameter permission_id |
