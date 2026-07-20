# Remove a custom field from a portfolio with Asana

Removes a custom field from a portfolio in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/removeCustomFieldSetting`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a custom field from a portfolio](https://developers.asana.com/reference/removecustomfieldsettingforportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.custom_field` | body | `string` | yes | — |
| `portfolio_gid` | path | `string` | yes | Asana portfolio gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `data.custom_field` | body | `string` | yes | Asana custom field parameter. |
