# List App Downloads with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/stats/:webzine_id/downloads/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List App Downloads](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | End date (included) with format %Y-%m-%d . Defaults to yesterday. |
| `platform` | query | `string` | no | Target platform. Defaults to "all". |
| `start_date` | query | `string` | no | Start date (included) with format %Y-%m-%d . Defaults to one month ago. |
