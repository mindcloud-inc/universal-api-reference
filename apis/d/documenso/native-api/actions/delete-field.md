# Delete Field with Documenso

Deletes an existing field from Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/field/delete`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Delete Field](https://docs.documenso.com/docs/developers/api/fields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fieldId` | body | `number` | yes |
