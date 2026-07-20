# Upload Files with HubSpot

Uploads a file to HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `files/v3/files`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Upload Files](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/basic/get-crm-v3-objects-contacts)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
| `folderPath` | body | `string` | yes |
| `options` | body | `string` | no |
