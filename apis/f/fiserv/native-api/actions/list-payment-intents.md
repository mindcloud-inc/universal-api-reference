# List Payment Intents with Fiserv

Retrieves payment intents for an account from Fiserv.

## Endpoint

- **Method:** `GET`
- **Path:** `/payment_intents`
- **Base URL:** `https://bankinghub-cert.fiservapis.com`
- **Official documentation:** [List Payment Intents](https://isvportal.fiserv.com/docs/payments-api#operation/get_payment_intents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `x-account-id` | body | `string` | yes | Fiserv account id sent in the required x-account-id header. |
