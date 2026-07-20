# Get Product Aggregate Statistics by Product ID with Shopper Approved

Retrieves product aggregate statistics from Shopper Approved by product ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregates/products/:siteid/:productid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [Get Product Aggregate Statistics by Product ID](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productid` | path | `number` | yes | The product ID or parent ID. |
