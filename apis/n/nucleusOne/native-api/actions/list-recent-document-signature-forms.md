# List Recent Document Signature Forms with Nucleus One

Retrieves recent document signature forms from Nucleus One.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/projects/:projectId/recentDocumentSignatureForms`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Recent Document Signature Forms](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `projectId` | path | `string` | yes | ID of the project |
| `cursor` | query | `string` | no | Pagination cursor. Leave empty to get the first page of results. |
| `nameFilter` | query | `string` | no | Filter forms by name |
| `excludingId` | query | `string` | no | Exclude form with this ID from results |
