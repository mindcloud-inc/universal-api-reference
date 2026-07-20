# List Migrations with Porter

Retrieves migrations from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/migrations`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Migrations](https://docs.porter.run/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose migrations you want to list. |
