# List Audit Logs with Porter

Retrieves audit logs from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/audit-logs`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Audit Logs](https://docs.porter.run/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose audit logs you want to list. |
