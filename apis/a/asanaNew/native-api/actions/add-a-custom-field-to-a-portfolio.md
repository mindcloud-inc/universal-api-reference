# Add a custom field to a portfolio with Asana

Adds a custom field to a portfolio in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios/:portfolio_gid/addCustomFieldSetting`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a custom field to a portfolio](https://developers.asana.com/reference/addcustomfieldsettingforportfolio)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `data.custom_field` | body | `string` | yes |
| `data.insert_after` | body | `string` | yes |
| `data.insert_before` | body | `string` | yes |
| `data.is_important` | body | `boolean` | yes |
| `portfolio_gid` | path | `string` | yes |
