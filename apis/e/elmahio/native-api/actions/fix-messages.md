# Fix Messages with elmah.io

Marks messages as fixed in elmah.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/messages/:logId/_fix`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [Fix Messages](https://api.elmah.io/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the log containing the messages. |
| `query` | body | `string` | yes | Lucene query. |
