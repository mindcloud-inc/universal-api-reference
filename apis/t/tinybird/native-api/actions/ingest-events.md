# Ingest Events with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/events`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Ingest Events](https://www.tinybird.co/docs/api-reference/events-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-ndjson` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `events` | body | `string` | yes | NDJSON events, one JSON object per line |
| `name` | query | `string` | yes | Target data source name or ID |
