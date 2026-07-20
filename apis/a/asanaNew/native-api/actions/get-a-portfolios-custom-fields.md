# Get a portfolio's custom fields with Asana

Retrieves a portfolio's custom fields from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `portfolios/:portfolio_gid/custom_field_settings`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a portfolio's custom fields](https://developers.asana.com/reference/getcustomfieldsettingsforportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `portfolio_gid` | path | `string` | yes | Path parameter: portfolio_gid |
