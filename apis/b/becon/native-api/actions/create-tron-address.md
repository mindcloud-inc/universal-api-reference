# Create Tron Address with Becon

Creates a new Tron payment address in Becon.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/address`
- **Base URL:** `https://external-api.bcon.global/api`
- **Official documentation:** [Create Tron Address](https://bcon.global/integrations/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chain` | body | `string` | yes | The target blockchain for the payment address. |
| `external_id` | body | `string` | yes | The external reference ID for the address request. |
| `origin_amount` | body | `string` | yes | The fiat amount to convert into the destination address request. |
| `origin_currency` | body | `string` | yes | The fiat currency code for the requested payment amount. |
| `payment_currency` | body | `string` | yes | The cryptocurrency or token code to receive. |
