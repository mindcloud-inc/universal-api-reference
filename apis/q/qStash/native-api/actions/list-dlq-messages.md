# List DLQ Messages with QStash

Retrieves all dead-letter queue messages from QStash.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/dlq`
- **Base URL:** `https://qstash-eu-central-1.upstash.io`
- **Official documentation:** [List DLQ Messages](https://upstash.com/docs/qstash/api-refence/dlq/list-dlq-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `number` | no | Number of DLQ messages to return, up to 100. |
| `cursor` | query | `string` | no | Pagination cursor returned by a prior DLQ list response. |
| `responseStatus` | query | `number` | no | Filter by HTTP response status code of the last delivery attempt. |
| `order` | query | `list` | no | Sorting order for DLQ messages. Accepted values: `0`, `1`. |
