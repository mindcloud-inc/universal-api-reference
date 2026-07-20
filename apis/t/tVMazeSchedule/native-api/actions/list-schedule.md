# List Schedule with TVMaze Schedule

Retrieves the TV schedule from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedule`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Schedule](https://www.tvmaze.com/api#schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Optional ISO 3166-1 country code; defaults to US. |
| `date` | query | `string` | no | Schedule date in TVMaze YYYY-MM-DD format. |
