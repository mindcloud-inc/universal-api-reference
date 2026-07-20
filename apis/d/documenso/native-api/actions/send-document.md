# Send Document with Documenso

Sends an existing document in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/distribute`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Send Document](https://docs.documenso.com/docs/developers/api/documents)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelopeId` | body | `string` | yes |
| `meta` | body | `object` | no |
