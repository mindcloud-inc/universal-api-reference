# List Services with Porter

Retrieves services from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/services`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Services](https://docs.porter.run/applications/deploy/configuring-application-services)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose services you want to list. |
