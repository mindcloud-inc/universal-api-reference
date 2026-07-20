# Create Fields with Documenso

Creates fields in Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/field/create-many`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Create Fields](https://docs.documenso.com/docs/developers/api/fields)

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
