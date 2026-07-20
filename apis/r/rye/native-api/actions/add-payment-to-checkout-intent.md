# Add Payment To Checkout Intent with Rye

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/checkout-intents/{id}/payment`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Add Payment To Checkout Intent](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The checkout intent id. |
| `paymentMethod` | body | `object` | yes | Payment method object. |
