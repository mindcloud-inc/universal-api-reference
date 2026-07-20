# Update Document with Documenso

Updates an existing document in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/update`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Update Document](https://docs.documenso.com/docs/developers/api/documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelopeId` | body | `string` | yes |
| `data` | body | `object` | no |
| `meta` | body | `object` | no |
