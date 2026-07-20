# Purchase Product with Rye

Creates a product purchase in Rye.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/checkout-intents/purchase`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Purchase Product](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer` | body | `object` | yes | Buyer information object. |
| `constraints` | body | `object` | no | Checkout constraints object. |
| `discoverPromoCodes` | body | `boolean` | no | Whether to discover promo codes automatically. |
| `paymentMethod` | body | `object` | yes | Payment method object. |
| `productUrl` | body | `string` | yes | Product URL to purchase. |
| `promoCodes[]` | body | `array<string>` | no | Promo codes to apply. Send multiple values as a array. |
| `quantity` | body | `number` | yes | Quantity to purchase. |
| `variantSelections[]` | body | `array<object>` | no | Variant selections to apply. Send multiple values as a array. |
