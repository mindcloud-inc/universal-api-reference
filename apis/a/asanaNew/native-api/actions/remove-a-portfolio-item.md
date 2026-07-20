# Remove a portfolio item with Asana

Removes an item from an Asana portfolio.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/removeItem`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a portfolio item](https://developers.asana.com/reference/removeitemforportfolio)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.item` | body | `string` | yes |
| `portfolio_gid` | path | `string` | yes |
