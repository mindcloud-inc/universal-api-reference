# Delete Template with Documenso

Deletes an existing template from Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/delete`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Delete Template](https://docs.documenso.com/docs/developers/api/templates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `number` | yes |
