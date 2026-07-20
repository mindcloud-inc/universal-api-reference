# Get Pricing with Seven

Retrieves pricing information from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/pricing`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Get Pricing](https://docs.seven.io/en/rest-api/endpoints/account#prices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country Code according to ISO-3166 (ALPHA-2) for which you want to query the prices. If this parameter is not specified, the prices of all countries are displayed. |
| `format` | query | `string` | yes | By default, the data is returned as JSON. However, you can also request a CSV format. To do this, use the parameter format=csv |
