# Create Charge with OPN

Creates a new charge in OPN.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges`
- **Base URL:** `https://api.omise.co`
- **Official documentation:** [Create Charge](https://docs.omise.co/charge-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `number` | yes | The charge amount in the smallest currency unit. |
| `capture` | body | `boolean` | no | Whether to capture the charge immediately. |
| `currency` | body | `string` | yes | The three-letter currency code. |
| `customer` | body | `string` | no | The customer ID to charge. |
| `description` | body | `string` | no | The charge description. |
