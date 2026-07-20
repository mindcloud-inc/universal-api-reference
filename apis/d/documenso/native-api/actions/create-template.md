# Create Template with Documenso

Creates a new template in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/create`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Create Template](https://docs.documenso.com/docs/developers/api/teams)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `payload` | body | `object` | yes |
| `file` | body | `file` | yes |
