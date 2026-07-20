# List Messages with elmah.io

Retrieves messages from a log in elmah.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/messages/:logId`
- **Base URL:** `https://api.elmah.io`
- **Official documentation:** [List Messages](https://docs.elmah.io/using-the-rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | A start date and time to search from. |
| `includeHeaders` | query | `boolean` | no | Include headers like server variables and cookies in the result. |
| `logId` | path | `string` | yes | The ID of the log containing the messages. |
| `pageIndex` | query | `number` | no | The page number of the result. |
| `pageSize` | query | `number` | no | The number of messages to load, max 100. |
| `query` | query | `string` | no | A full-text or Lucene query to limit the messages by. |
| `searchAfter` | query | `string` | no | Continue from the end of the previous search result. |
| `to` | query | `string` | no | An end date and time to search to. |
