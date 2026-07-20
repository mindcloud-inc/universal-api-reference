# List Stripe Charges with Beds24

Retrieves Stripe charges for a booking from Beds24.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/stripe/charges`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Stripe Charges](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | query | `number` | yes | Beds24 booking ID whose Stripe charges should be listed. |
