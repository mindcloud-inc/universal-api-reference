# Fetch Gas Price with Poof

Retrieves current gas price data from Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/gas_price`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Fetch Gas Price](https://docs.poof.io/reference/fetchgasprice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crypto` | body | `string` | yes | Crypto asset code. |
