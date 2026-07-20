# List Stripe Payment Methods with Beds24

Retrieves Stripe payment methods for a booking from Beds24.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels/stripe/paymentMethods`
- **Base URL:** `https://beds24.com/api/v2`
- **Official documentation:** [List Stripe Payment Methods](https://wiki.beds24.com/index.php/API_V2.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bookingId` | query | `number` | yes | Beds24 booking ID whose Stripe payment methods should be listed. |
