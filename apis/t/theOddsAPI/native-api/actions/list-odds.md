# List Odds with The Odds

Retrieves odds for sports events from The Odds API.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/sports/:sport/odds/`
- **Base URL:** `https://api.the-odds-api.com`
- **Official documentation:** [List Odds](https://the-odds-api.com/liveapi/guides/v4/#get-odds)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookmakers` | query | `string` | no | Optional comma-separated bookmaker keys. Overrides regions when supplied. |
| `dateFormat` | query | `string` | no | Optional timestamp format, unix or iso. |
| `markets` | query | `string` | no | Optional comma-separated market keys such as h2h or spreads. |
| `oddsFormat` | query | `string` | no | Optional odds format such as american or decimal. |
| `regions` | query | `string` | yes | Comma-separated regions to include, for example us or us,uk. |
| `sport` | path | `string` | yes | The sport key returned by List Sports. |
