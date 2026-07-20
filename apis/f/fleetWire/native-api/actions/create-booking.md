# Create Booking with FleetWire

Creates a new booking in FleetWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/checkout`
- **Base URL:** `https://api.fleetwire.io`
- **Official documentation:** [Create Booking](https://documenter.getpostman.com/view/263138/Tz5p6dWS)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `version` | body | `string` | yes | FleetWire checkout API version. |
| `l_id` | body | `string` | yes | FleetWire listing ID for the booking. |
| `dates.start` | body | `string` | yes | Checkout start datetime. |
| `dates.end` | body | `string` | yes | Checkout end datetime. |
| `customers[0].firstName` | body | `string` | yes | Primary customer first name. |
| `customers[0].lastName` | body | `string` | yes | Primary customer last name. |
| `customers[0].email` | body | `string` | yes | Primary customer email. |
| `customers[0].phone` | body | `string` | yes | Primary customer phone number. |
| `customers[0].isPrimary` | body | `boolean` | yes | Whether this customer is the primary renter. |
| `customers[0].phone_number` | body | `string` | yes | Primary customer phone number in the phone_number field. |
| `customers[0].agreeToS` | body | `boolean` | yes | Whether the customer agrees to the terms. |
| `customers[0].dob` | body | `string` | yes | Primary customer date of birth in YYYY-MM-DD format. |
| `customers[0].age` | body | `string` | no | Primary customer age if required by the tenant checkout validation. |
