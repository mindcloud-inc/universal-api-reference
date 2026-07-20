# Get Product Aggregate Statistics with Shopper Approved

Retrieves product aggregate statistics from Shopper Approved.

## Endpoint

- **Method:** `GET`
- **Path:** `/aggregates/products/:siteid`
- **Base URL:** `https://api.shopperapproved.com/`
- **Official documentation:** [Get Product Aggregate Statistics](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by_match_key` | query | `boolean` | no | Whether to group product aggregates by a matching key like SKU or MPN. |
| `siteOnly` | query | `boolean` | no | Whether to return only the site_totals object. |
| `fastmode` | query | `boolean` | no | Whether to use the optimized fastmode query. |
