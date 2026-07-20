# Confirm Checkout Intent with Rye

Confirms a checkout intent in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/checkout-intents/{id}/confirm`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Confirm Checkout Intent](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The checkout intent id. |
| `paymentMethod` | body | `object` | yes | Payment method object. |
