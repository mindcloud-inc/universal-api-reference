# Add users to a portfolio with Asana

Adds users to a portfolio in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/addMembers`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add users to a portfolio](https://developers.asana.com/reference/addmembersforportfolio)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.members` | body | `string` | yes |
| `portfolio_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
