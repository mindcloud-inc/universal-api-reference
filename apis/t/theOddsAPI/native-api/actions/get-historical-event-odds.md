# Get Historical Event Odds with The Odds

Retrieves historical odds for a specific event from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/historical/sports/:sport/events/:eventId/odds`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [Get Historical Event Odds](https://the-odds-api.com/liveapi/guides/v4/#get-historical-event-odds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmakers` | query | `string` | no | Optional comma-separated bookmaker keys. Overrides regions when supplied. |
| `date` | query | `string` | yes | Historical snapshot timestamp in ISO 8601 format. |
| `dateFormat` | query | `string` | no | Optional timestamp format, unix or iso. |
| `eventId` | path | `string` | yes | The event id returned by List Historical Events or the provider snapshot. |
| `markets` | query | `string` | no | Optional comma-separated market keys. |
| `oddsFormat` | query | `string` | no | Optional odds format such as american or decimal. |
| `regions` | query | `string` | yes | Comma-separated regions to include, for example us or us,uk. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
