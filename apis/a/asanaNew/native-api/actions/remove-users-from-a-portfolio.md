# Remove users from a portfolio with Asana

Removes users from an Asana portfolio.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/removeMembers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove users from a portfolio](https://developers.asana.com/reference/removemembersforportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.members` | body | `string` | yes | — |
| `opt_fields[]` | query | `array<string>` | no | — |
| `portfolio_gid` | path | `string` | yes | Path parameter: portfolio_gid |
| `data` | body | `object` | yes | — |
