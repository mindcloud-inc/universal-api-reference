# Update Comment with Wrike

Updates an existing comment in Wrike.

## Endpoint

- **Method:** `PUT`
- **Path:** `/comments/:commentId`
- **Base URL:** `https://{host}/api/v4`
- **Official documentation:** [Update Comment](https://developers.wrike.com/api/v4/comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | Wrike comment ID. |
| `text` | query | `string` | yes | Comment text, cannot be empty |
| `plainText` | query | `boolean` | no | Treat comment text as plain text |
