# Create Messages Bulk with elmah.io

Creates one or more messages in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages/:logId/_bulk`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Create Messages Bulk](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log which should contain the new messages. |
| `messages[]` | body | `array<object>` | yes | The messages to create. |
| `title` | body | `string` | yes | The textual title or headline of each message to log. |
