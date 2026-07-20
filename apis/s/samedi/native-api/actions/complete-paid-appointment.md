# Complete Paid Appointment with Samedi

Completes a paid appointment booking in Samedi.

## Endpoint

- **Method:** `POST`
- **Path:** `/booking/v3/book`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [Complete Paid Appointment](https://api-docs.samedi.de/booking-api/appointment-booking/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_url` | body | `string` | yes | PayPal order URL in the documented samedi format. |
| `billing_information[first_name]` | body | `string` | yes | Billing first name. |
| `billing_information[last_name]` | body | `string` | yes | Billing last name. |
| `billing_information[street]` | body | `string` | yes | Billing street address. |
| `billing_information[city]` | body | `string` | yes | Billing city. |
| `billing_information[country]` | body | `string` | yes | Billing country as ISO 3166-1 alpha-2 code. |
| `billing_information[zip]` | body | `string` | yes | Billing ZIP or postal code. |
| `billing_information[email]` | body | `string` | yes | Billing email address. |
| `event_category_id` | body | `string` | yes | Appointment category ID for the paid booking. |
| `event_type_id` | body | `string` | yes | Appointment type ID for the paid booking. |
| `starts_at` | body | `string` | yes | Selected appointment start timestamp for the paid booking. |
