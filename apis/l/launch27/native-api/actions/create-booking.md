# Create Booking with Launch27

Creates a new booking in Launch27.

## Endpoint

- **Method:** `POST`
- **Path:** `booking`
- **Base URL:** `https://{subdomain}.launch27.com/v1`
- **Official documentation:** [Create Booking](https://api.launch27.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `object` | yes | Launch27 booking user object containing first_name, last_name, and email. |
| `address` | body | `string` | yes | Booking street address. |
| `city` | body | `string` | yes | Booking city. |
| `state` | body | `string` | yes | Booking state or region. |
| `zip` | body | `string` | yes | Booking postal code. |
| `phone` | body | `string` | yes | Booking phone number. |
| `location_id` | body | `number` | yes | Launch27 location ID for the booking. |
| `frequency_id` | body | `number` | yes | Launch27 frequency ID for the booking. |
| `service_date` | body | `string` | yes | Booking service date-time in Launch27 backend format YYYY-MM-DDTHH:mm:ss. |
| `arrival_window` | body | `number` | yes | Arrival window in minutes. |
| `services` | body | `list<object>` | yes | Selected Launch27 booking services array. |
| `payment_method` | body | `string` | yes | Booking payment method such as cash, check, paypal, stripe, or fspay. |
| `custom_fields` | body | `list<object>` | no | Optional Launch27 booking custom fields array. |
