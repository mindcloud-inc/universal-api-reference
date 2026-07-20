# List Web Schedule with TVMaze Schedule

Retrieves the web streaming schedule from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/schedule/web`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Web Schedule](https://www.tvmaze.com/api#web-streaming-schedule)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | no | Optional ISO 3166-1 country code; omit for all web channels or send empty string for global web channels. |
| `date` | query | `string` | no | Web schedule date in TVMaze YYYY-MM-DD format. |
