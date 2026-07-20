# Create Checkout Intent with Rye

Creates a checkout intent in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/checkout-intents`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Create Checkout Intent](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer` | body | `object` | yes | Buyer information object. |
| `constraints` | body | `object` | no | Checkout constraints object. |
| `discoverPromoCodes` | body | `boolean` | no | Whether to discover promo codes automatically. |
| `productUrl` | body | `string` | yes | Product URL to purchase. |
| `promoCodes[]` | body | `array<string>` | no | Promo codes to apply. Send multiple values as a array. |
| `quantity` | body | `number` | yes | Quantity to purchase. |
| `variantSelections[]` | body | `array<object>` | no | Variant selections to apply. Send multiple values as a array. |
