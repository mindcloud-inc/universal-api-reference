# Create Message with elmah.io

Creates a new message in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages/:logId`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Create Message](https://docs.elmah.io/using-the-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | no | The ID of the log which should contain the new message. |
| `title` | body | `string` | yes | The textual title or headline of the message to log. |
