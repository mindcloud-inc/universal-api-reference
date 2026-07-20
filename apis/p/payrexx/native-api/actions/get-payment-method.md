# Get Payment Method with Payrexx

Retrieves a payment method from Payrexx.

## Endpoint

- **Method:** `GET`
- **Path:** `PaymentMethod/:paymentMethod/`
- **Base URL:** `https://api.payrexx.com/v1.14/`
- **Official documentation:** [Get Payment Method](https://developers.payrexx.com/reference/get-one-payment-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `paymentMethod` | path | `string` | yes | ID of the payment method (e.g. twint or mastercard). |
