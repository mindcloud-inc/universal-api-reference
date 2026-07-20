# Create a payment intent with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/payment/stripe/payment-intent/create`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Create a payment intent](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quantity` | body | `number` | no | The number of credits being purchased |
