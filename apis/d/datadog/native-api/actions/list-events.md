# List Events with Datadog

Retrieves events from Datadog.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/events`
- **Base URL:** `https://api.us5.datadoghq.com`
- **Official documentation:** [List Events](https://docs.datadoghq.com/api/latest/events/#get-a-list-of-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `number` | yes | POSIX start timestamp. |
| `end` | query | `number` | yes | POSIX end timestamp. |
| `priority` | query | `string` | no | Event priority to filter by. |
| `sources` | query | `string` | no | Comma-separated event sources. |
| `tags` | query | `string` | no | Comma-separated tags for filtering events. |
| `unaggregated` | query | `boolean` | no | Return all events within the timeframe. |
| `exclude_aggregate` | query | `boolean` | no | Return only unaggregated events. |
| `page` | query | `number` | no | Page number when using unaggregated event pagination. |
