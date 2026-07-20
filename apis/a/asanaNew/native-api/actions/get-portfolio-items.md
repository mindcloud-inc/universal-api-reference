# Get portfolio items with Asana

Retrieves portfolio items from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `portfolios/:portfolio_gid/items`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get portfolio items](https://developers.asana.com/reference/getitemsforportfolio)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `portfolio_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
