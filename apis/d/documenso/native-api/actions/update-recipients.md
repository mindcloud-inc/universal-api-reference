# Update Recipients with Documenso

Updates existing recipients in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/recipient/update-many`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Update Recipients](https://docs.documenso.com/docs/developers/api/recipients)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelopeId` | body | `string` | yes |
| `data[]` | body | `array<object>` | yes |
