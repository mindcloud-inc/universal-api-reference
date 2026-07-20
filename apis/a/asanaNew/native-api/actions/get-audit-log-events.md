# Get audit log events with Asana

Retrieves audit log events from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspace_gid/audit_log_events`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get audit log events](https://developers.asana.com/reference/getauditlogevents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_gid` | path | `string` | yes |
