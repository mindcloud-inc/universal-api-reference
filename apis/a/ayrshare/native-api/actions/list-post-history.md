# List Post History with Ayrshare

Retrieves post history from Ayrshare.

## Endpoint

- **Method:** `GET`
- **Path:** `/history`
- **Base URL:** `https://api.ayrshare.com/api`
- **Official documentation:** [List Post History](https://www.ayrshare.com/docs/apis/history/get-history)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lastDays` | query | `number` | no | Return posts from the last number of days. Use 0 to return all history constrained by the limit. |
| `platforms[]` | query | `array<string>` | no | Filter by one or more Ayrshare platform values. |
| `status` | query | `string` | no | Filter by post status such as success, error, pending, paused, deleted, or awaiting approval. Accepted values: `awaiting approval`, `deleted`, `error`, `paused`, `pending`, `processing`, `success`. |
