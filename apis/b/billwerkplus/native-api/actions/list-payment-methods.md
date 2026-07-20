# List Payment Methods with Billwerkplus

Retrieves payment methods from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/payment_method`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Payment Methods](https://docs.frisbii.com/reference/getpaymentmethodlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer` | query | `string` | no | Customer handle filter. |
| `state[]` | query | `array<string>` | no | Payment method states to include. Multiple values are allowed. Send multiple values as a array. |
| `payment_type[]` | query | `array<string>` | no | Payment types to include. Multiple values are allowed. Send multiple values as a array. |
| `reference` | query | `string` | no | Payment method reference filter. |
| `id` | query | `string` | no | Exact payment method id. |
| `offline_agreement_handle` | query | `string` | no | Offline agreement handle filter. |
