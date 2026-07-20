# Create Checkout with Poof

Creates a new checkout in Poof.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.poof.io/api/v1/checkout`
- **Base URL:** `https://www.poof.io/api/v2`
- **Official documentation:** [Create Checkout](https://docs.poof.io/reference/poof-checkout)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Checkout username from the Poof docs example. |
| `amount` | body | `string` | yes | Checkout amount. |
