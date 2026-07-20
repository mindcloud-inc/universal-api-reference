# Search Videos And Channels with Invidious

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [Search Videos And Channels](https://docs.invidious.io/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | no | Search date filter: hour, today, week, month, or year. |
| `duration` | query | `string` | no | Search duration filter: short, medium, or long. |
| `features` | query | `string` | no | Comma-separated search features such as hd, subtitles, 3d, live, or 4k. Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | Search result page number. |
| `q` | query | `string` | yes | Search text. |
| `region` | query | `string` | no | ISO 3166 country code. |
| `sort` | query | `string` | no | Search sort: relevance or views. |
| `type` | query | `string` | no | Search result type: video, playlist, channel, movie, show, or all. |
