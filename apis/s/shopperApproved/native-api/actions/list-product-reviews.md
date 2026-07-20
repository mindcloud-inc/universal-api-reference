# List Product Reviews with Shopper Approved

Retrieves product reviews from Shopper Approved.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/reviews/:siteid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [List Product Reviews](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | The first date in YYYY-MM-DD format. |
| `to` | query | `date` | no | The last date in YYYY-MM-DD format. |
| `sort` | query | `string` | no | How the reviews should be sorted. |
| `removed` | query | `number` | no | Whether to include removed reviews. |
