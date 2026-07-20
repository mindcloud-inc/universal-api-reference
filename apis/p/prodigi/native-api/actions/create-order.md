# Create Order with Prodigi

Creates and submits a new order in Prodigi.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [Create Order](https://www.prodigi.com/print-api/docs/reference/#create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shippingMethod` | body | `string` | yes | Requested shipping method: budget, standard, standardplus, express, overnight. |
| `recipient` | body | `object` | yes | Recipient object including name and address. |
| `items[]` | body | `array<object>` | yes | Array of order items. Each item includes sku, copies, sizing, and assets. |
| `merchantReference` | body | `string` | no | Your reference for this order. |
| `callbackUrl` | body | `string` | no | URL Prodigi can call with order progress callbacks. |
| `idempotencyKey` | body | `string` | no | Unique key that helps Prodigi detect duplicate order submissions. |
| `metadata` | body | `object` | no | Custom metadata object stored with the order. |
| `branding` | body | `object` | no | Optional branding assets such as postcard, flyer, packing slip, or stickers. |
| `packingSlip` | body | `object` | no | Optional packing slip object. |
