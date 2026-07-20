# Get Conversions with Api2Convert

Retrieves valid conversion types from Api2Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversions`
- **Base URL:** `https://api.api2convert.com/v2`
- **Official documentation:** [Get Conversions](https://api.api2convert.com/v2/schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter available conversions by category. |
| `target` | query | `string` | no | Filter available conversions by target format. |
| `page` | query | `string` | no | Page number for paginated conversion results. |
