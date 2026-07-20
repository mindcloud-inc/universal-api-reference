# List Build Settings with Porter

Retrieves build settings from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/build-settings`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Build Settings](https://docs.porter.run/applications/deploy/builds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose build settings you want to list. |
