# Add Payment Method with Reepay

Adds a payment method in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payment_method`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Add Payment Method](https://docs.frisbii.com/reference/addpaymentmethodv2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | body | `object` | no | — |
| `customer_handle` | body | `string` | no | — |
| `reference` | body | `string` | no | — |
| `source` | body | `string` | yes | The payment method source, for example a one-time card token like ct_f96004cae4308473c92bea0638b5b688. |
