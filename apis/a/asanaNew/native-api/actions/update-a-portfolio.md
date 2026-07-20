# Update a portfolio with Asana

Updates a portfolio in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `portfolios/:portfolio_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a portfolio](https://developers.asana.com/reference/updateportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | — |
| `portfolio_gid` | path | `string` | yes | Asana portfolio gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
