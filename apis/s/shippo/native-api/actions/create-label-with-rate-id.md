# Create Label with Rate ID with Shippo - Legacy

Creates a shipping label in Shippo from a rate ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions`
- **Base URL:** `https://api.goshippo.com`
- **Official documentation:** [Create Label with Rate ID](https://docs.goshippo.com/shippoapi/public-api/transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `async` | body | `boolean` | no | — |
| `rate` | body | `string` | no | — |
| `apiKey` | path | `string` | no | Override the authentication API key here |
