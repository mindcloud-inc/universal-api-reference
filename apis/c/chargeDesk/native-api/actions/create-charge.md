# Create Charge with ChargeDesk

Creates a new charge in ChargeDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/charges`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Create Charge](https://chargedesk.com/api-docs#charges-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amount` | body | `string` | yes | Decimal amount for the charge, without a currency symbol. |
| `currency` | body | `string` | yes | Three-letter currency code for the charge. |
| `customer[id]` | body | `string` | yes | Unique customer identifier for the charge. |
