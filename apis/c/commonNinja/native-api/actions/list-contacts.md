# List Contacts with Common Ninja

Retrieves project contacts from Common Ninja.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/contacts`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [List Contacts](https://developers.commoninja.com/docs/api/crm/contacts-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID. |
| `limit` | query | `number` | no | Maximum number of contacts to return. |
