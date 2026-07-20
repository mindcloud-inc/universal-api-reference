# Create a portfolio with Asana

Creates a portfolio in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `portfolios`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Create a portfolio](https://developers.asana.com/reference/createportfolio)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
