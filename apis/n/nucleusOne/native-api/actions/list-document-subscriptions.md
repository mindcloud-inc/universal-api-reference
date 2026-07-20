# List Document Subscriptions with Nucleus One

Retrieves document subscriptions from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/documentSubscriptions`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Document Subscriptions](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
