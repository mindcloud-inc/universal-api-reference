# Add Offline Payment Method with Reepay

Adds an offline payment method in Reepay.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/payment_method/offline`
- **Base URL:** `https://api.frisbii.com`
- **Official documentation:** [Add Offline Payment Method](https://docs.frisbii.com/reference/addofflinepaymentmethod)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_handle` | body | `string` | no | — |
| `offline_agreement_handle` | body | `string` | yes | The unique offline agreement handle per account, for example offline-cash-dkk-1. |
| `reference` | body | `string` | no | — |
