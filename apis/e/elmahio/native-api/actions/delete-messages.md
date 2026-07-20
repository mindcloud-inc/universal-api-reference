# Delete Messages with elmah.io

Deletes messages from a log in elmah.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/messages/:logId`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Delete Messages](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log containing the messages. |
| `query` | body | `string` | yes | Lucene query. |
