# List Product Reviews by Product or Parent ID with Shopper Approved

Retrieves product reviews from Shopper Approved by product ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/reviews/:siteid/:productid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [List Product Reviews by Product or Parent ID](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productid` | path | `string` | yes | The product ID or parent ID. |
| `from` | query | `date` | no | The first date in YYYY-MM-DD format. |
| `to` | query | `date` | no | The last date in YYYY-MM-DD format. |
| `sort` | query | `string` | no | How the reviews should be sorted. |
| `removed` | query | `number` | no | Whether to include removed reviews. |
