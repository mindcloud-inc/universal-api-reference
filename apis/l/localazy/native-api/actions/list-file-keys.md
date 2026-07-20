# List File Keys with Localazy

Retrieves file keys for a project file in Localazy.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/files/:fileId/keys/:lang`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [List File Keys](https://localazy.com/docs/api/files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project id. |
| `fileId` | path | `string` | yes | Localazy file id. |
| `lang` | path | `string` | yes | Locale code in ll-Scrp-RR format. |
| `deprecated` | query | `boolean` | no | Include deprecated keys. |
| `limit` | query | `number` | no | Number of keys to return per page. |
| `next` | query | `string` | no | Cursor for the next page of keys. |
| `extra_info` | query | `boolean` | no | Include hidden, limit, deprecated, and comment metadata. |
| `no_content` | query | `boolean` | no | Skip translation content values in the response. |
