# List Payment Method Intents with Fiserv

Retrieves payment method intents from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_method_intents`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Payment Method Intents](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_method_intents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
