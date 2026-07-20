# List Task Subscriptions with Nucleus One

Retrieves task subscriptions from a Nucleus One project.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/taskSubscriptions`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Task Subscriptions](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
