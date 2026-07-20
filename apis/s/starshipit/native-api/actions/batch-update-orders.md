# Batch Update Orders with Starshipit

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/batchupdate`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Batch Update Orders](https://api-docs.starshipit.com/#8cb8c76d-16e0-4465-b07c-8355d5c012af)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_ids[]` | body | `array<number>` | no |
| `product_code` | body | `string` | no |
| `carrier_id` | body | `string` | no |
