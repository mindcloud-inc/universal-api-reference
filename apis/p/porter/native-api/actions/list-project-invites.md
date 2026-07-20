# List Project Invites with Porter

Retrieves invites from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/invites`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Project Invites](https://docs.porter.run/security-and-compliance/role-based-access-control)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose invites you want to list. |
