# Delete Document with Documenso

Deletes an existing document from Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/delete`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Delete Document](https://docs.documenso.com/docs/developers/api/documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelopeId` | body | `string` | yes |
