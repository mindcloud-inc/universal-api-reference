# Add a portfolio item with Asana

Adds an item to a portfolio in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/addItem`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a portfolio item](https://developers.asana.com/reference/additemforportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `data.insert_after` | body | `string` | yes | — |
| `data.insert_before` | body | `string` | yes | — |
| `data.item` | body | `string` | yes | — |
| `portfolio_gid` | path | `string` | yes | Path parameter: portfolio_gid |
