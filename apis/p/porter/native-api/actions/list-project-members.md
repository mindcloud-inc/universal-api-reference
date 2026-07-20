# List Project Members with Porter

Retrieves members from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/members`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Project Members](https://docs.porter.run/security-and-compliance/role-based-access-control)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose collaborators you want to list. |
