# List Events with The Odds

Retrieves sports events from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/sports/:sport/events`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [List Events](https://the-odds-api.com/liveapi/guides/v4/#get-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFormat` | query | `string` | no | Optional timestamp format, unix or iso. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
