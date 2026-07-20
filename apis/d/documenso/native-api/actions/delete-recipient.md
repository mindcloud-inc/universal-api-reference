# Delete Recipient with Documenso

Deletes an existing recipient from Documenso.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/recipient/delete`
- **Base URL:** `https://app.documenso.com/api/v2`
- **Official documentation:** [Delete Recipient](https://docs.documenso.com/docs/developers/api/recipients)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recipientId` | body | `number` | yes |
