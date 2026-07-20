# List Historical Events with The Odds

Retrieves historical events from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/historical/sports/:sport/events`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [List Historical Events](https://the-odds-api.com/liveapi/guides/v4/#get-historical-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | query | `string` | yes | Historical snapshot timestamp in ISO 8601 format. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
