# Delete Message with elmah.io

Deletes an existing message from elmah.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/messages/:logId/:id`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Delete Message](https://docs.elmah.io/using-the-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | The ID of the message to delete. |
| `logId` | path | `string` | no | The ID of the log containing the message. |
