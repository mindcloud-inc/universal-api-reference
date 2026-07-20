# Get Event Markets with The Odds

Retrieves markets for a specific event from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/sports/:sport/events/:eventId/markets`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [Get Event Markets](https://the-odds-api.com/liveapi/guides/v4/#get-event-markets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmakers` | query | `string` | no | Optional comma-separated bookmaker keys. Overrides regions when supplied. |
| `dateFormat` | query | `string` | no | Optional timestamp format, unix or iso. |
| `eventId` | path | `string` | yes | The event id returned by List Events. |
| `regions` | query | `string` | yes | Comma-separated regions to include, for example us or us,uk. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
