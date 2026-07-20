# Get Message with elmah.io

Retrieves a message from elmah.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/messages/:logId/:id`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Get Message](https://docs.elmah.io/using-the-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the message to fetch. |
| `logId` | path | `string` | yes | The ID of the log containing the message. |
