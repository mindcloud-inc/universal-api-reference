# List Environment Groups with Porter

Retrieves environment groups from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/alpha/projects/:projectId/cloud-environment-groups`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Environment Groups](https://docs.porter.run/applications/configure/environment-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose environment groups you want to list. |
