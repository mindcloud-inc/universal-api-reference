# List Brands with Giftbit

Lists available reward brands in Giftbit.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands`
- **Base URL:** `https://api-testbed.giftbit.com/papi/v1`
- **Official documentation:** [List Brands](https://www.giftbit.com/api-documentation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `region` | query | `number` | no |
| `search` | query | `string` | no |
| `currencyisocode` | query | `string` | no |
| `embeddable` | query | `boolean` | no |
| `min_price_in_cents` | query | `number` | no |
| `max_price_in_cents` | query | `number` | no |
