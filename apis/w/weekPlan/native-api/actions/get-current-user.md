# Get Current User with Week Plan

## Endpoint

- **Method:** `GET`
- **Path:** `users`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Get Current User](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Day` | query | `number` | yes | Calendar day used by the Week Plan user endpoint. |
| `Month` | query | `number` | yes | Calendar month used by the Week Plan user endpoint. |
| `Timezone` | query | `number` | yes | Timezone offset in minutes used by the Week Plan user endpoint. |
| `TzName` | query | `string` | yes | IANA timezone name used by the Week Plan user endpoint. |
| `Year` | query | `number` | yes | Calendar year used by the Week Plan user endpoint. |
