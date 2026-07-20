# List Participants with The Odds

Retrieves participants for a sport from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/sports/:sport/participants`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [List Participants](https://the-odds-api.com/liveapi/guides/v4/#get-participants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
