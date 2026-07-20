# Fix Message with elmah.io

Marks a message as fixed in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages/:logId/:id/_fix`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Fix Message](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log containing the message. |
| `id` | path | `string` | yes | The ID of the message to fix. |
| `markAllAsFixed` | query | `boolean` | no | If true, all instances of the log message are set to fixed. |
