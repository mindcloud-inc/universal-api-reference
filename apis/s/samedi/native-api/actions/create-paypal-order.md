# Create PayPal Order with Samedi

Creates a PayPal order in Samedi.

## Endpoint

- **Method:** `POST`
- **Path:** `/automated_payment/v1/orders`
- **Base URL:** `https://patient.samedi.de/api`
- **Official documentation:** [Create PayPal Order](https://api-docs.samedi.de/booking-api/appointment-booking/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type_id` | body | `string` | yes | Appointment type ID used to generate the PayPal Order ID. |
