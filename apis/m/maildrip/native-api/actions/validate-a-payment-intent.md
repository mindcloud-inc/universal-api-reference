# Validate a payment intent with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment/stripe/payment-intent/validate`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Validate a payment intent](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentIntentId` | body | `string` | no | The ID of the payment intent to validate |
