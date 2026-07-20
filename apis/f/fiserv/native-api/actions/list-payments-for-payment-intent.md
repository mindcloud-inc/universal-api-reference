# List Payments For Payment Intent with Fiserv

Retrieves payments for a payment intent from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_intents/{id}/payments`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Payments For Payment Intent](https://isvportal.fiserv.com/docs/payments-api#operation/list_payments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | path | `string` | yes | Payment intent id from the path. |
