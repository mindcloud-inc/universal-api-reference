# Create Billing Contact with CoinGate

Creates a new billing contact in CoinGate.

## Endpoint

- **Method:** `POST`
- **Path:** `/billing/contacts`
- **Base URL:** `https://api.coingate.com/api/v2`
- **Official documentation:** [Create Billing Contact](https://developer.coingate.com/reference/create-billing-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_type` | body | `string` | yes | Billing contact type. |
| `email` | body | `string` | yes | Billing contact email. |
