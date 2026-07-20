# Hide Message with elmah.io

Hides a message in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages/:logId/:id/_hide`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Hide Message](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log containing the message. |
| `id` | path | `string` | yes | The ID of the message to hide. |
