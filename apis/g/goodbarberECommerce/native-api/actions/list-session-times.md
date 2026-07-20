# List Session Times with Goodbarber eCommerce

## Endpoint

- **Method:** `GET`
- **Path:** `/publicapi/v2/general/stats/:webzine_id/session_time/`
- **Base URL:** `https://commerce.goodbarber.dev`
- **Official documentation:** [List Session Times](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | End date (included) with format %Y-%m-%d . Defaults to yesterday. |
| `start_date` | query | `string` | no | Start date (included) with format %Y-%m-%d . Defaults to one month ago. |
