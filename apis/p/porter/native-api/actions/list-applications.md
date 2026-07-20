# List Applications with Porter

Retrieves applications from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/apps`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Applications](https://docs.porter.run/standard/cli/command-reference/porter-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose applications you want to list. |
