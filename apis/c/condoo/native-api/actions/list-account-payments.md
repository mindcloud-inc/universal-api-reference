# List Account Payments with condoo

Retrieves account payments from condoo.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [List Account Payments](https://trk.condoo.systems/en/api-documentation/payments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `frequency` | query | `string` | no | Optional payment frequency selector. |
| `processor` | query | `string` | no | Optional payment processor selector. |
| `status` | query | `string` | no | Optional payment status selector. |
| `type` | query | `string` | no | Optional payment type selector. |
