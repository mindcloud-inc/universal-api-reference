# Create Payment with TrueLayer

Creates a payment in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Create Payment](https://docs.truelayer.com/reference/create-payment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | JSON request body. Required fields: amount_in_minor, currency, payment_method, and user. |
