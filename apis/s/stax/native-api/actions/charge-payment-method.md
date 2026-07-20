# Charge Payment Method with Stax

Charges a payment method in Stax.

## Endpoint

- **Method:** `POST`
- **Path:** `/charge`
- **Base URL:** `https://apiprod.fattlabs.com`
- **Official documentation:** [Charge Payment Method](https://docs.staxpayments.com/reference/charge-a-payment-method)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `meta` | body | `object` | no | Charge metadata |
| `payment_method_id` | body | `string` | no | Payment method identifier |
| `pre_auth` | body | `boolean` | no | Pre-authorization flag |
| `total` | body | `number` | no | Charge total in dollars |
