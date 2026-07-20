# Retrieve Log Entries with Algolia

Retrieves log entries from the Algolia application.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/logs`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve Log Entries](https://www.algolia.com/doc/rest-api/search/get-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Position of the first log entry to retrieve. |
| `length` | query | `number` | no | Maximum number of log entries to retrieve. |
| `type` | query | `string` | no | Log entry type to filter by. |
| `indexName` | query | `string` | no | Index name to filter logs by. |
