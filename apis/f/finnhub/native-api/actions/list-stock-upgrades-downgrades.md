# List Stock Upgrades Downgrades with Finnhub

Retrieves stock upgrades and downgrades from Finnhub.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock/upgrade-downgrade`
- **Base URL:** `https://finnhub.io/api/v1`
- **Official documentation:** [List Stock Upgrades Downgrades](https://finnhub.io/docs/api#upgrade-downgrade)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `symbol` | query | `string` | no | Optional company symbol. Leave blank for latest upgrades and downgrades. |
| `from` | query | `string` | no | Start date in YYYY-MM-DD format. |
| `to` | query | `string` | no | End date in YYYY-MM-DD format. |
