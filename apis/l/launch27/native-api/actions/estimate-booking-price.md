# Estimate Booking Price with Launch27

Retrieves a booking price estimate from Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `booking/estimate_price`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Estimate Booking Price](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_id` | body | `number` | yes | Launch27 location ID for the booking estimate. |
| `frequency_id` | body | `number` | yes | Launch27 booking frequency ID. |
| `service_date` | body | `string` | yes | Service date-time in Launch27 backend format YYYY-MM-DDTHH:mm:ss. |
| `services` | body | `list<object>` | yes | Array of selected Launch27 booking services. |
| `email` | body | `string` | no | Customer email for estimate validation and discount logic. |
| `tip` | body | `number` | no | Optional tip amount. |
| `discount_code` | body | `string` | no | Optional booking discount code. |
| `quote_uuid` | body | `string` | no | Optional Launch27 quote UUID to estimate from. |
