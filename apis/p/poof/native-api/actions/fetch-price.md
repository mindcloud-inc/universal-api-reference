# Fetch Price with Poof

Retrieves a price quote from Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `/price`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Fetch Price](https://docs.poof.io/reference/fetchprice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crypto` | body | `string` | yes | Cryptocurrency or token symbol to price, for example bitcoin. |
