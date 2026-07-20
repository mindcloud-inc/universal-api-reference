# List Coins with Minerstat

Retrieves coins from the Minerstat catalog.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/coins`
- **Base URL:** `https://api.minerstat.com`
- **Official documentation:** [List Coins](https://api.minerstat.com/docs-coins/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | no | Comma-separated coin tickers like BTC,BCH,BSV. |
| `algo` | query | `string` | no | Comma-separated algorithms like SHA-256,Scrypt. |
