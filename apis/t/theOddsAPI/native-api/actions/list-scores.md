# List Scores with The Odds

Retrieves scores for sports events from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/sports/:sport/scores/`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [List Scores](https://the-odds-api.com/liveapi/guides/v4/#get-scores)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFormat` | query | `string` | no | Optional timestamp format, unix or iso. |
| `daysFrom` | query | `string` | no | Optional number of days from now to include in scores. |
| `eventIds` | query | `string` | no | Optional comma-separated event ids to filter scores. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
