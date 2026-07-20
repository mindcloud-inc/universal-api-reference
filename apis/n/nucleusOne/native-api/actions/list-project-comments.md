# List Project Comments with Nucleus One

Retrieves project comments from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/comments`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Project Comments](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
