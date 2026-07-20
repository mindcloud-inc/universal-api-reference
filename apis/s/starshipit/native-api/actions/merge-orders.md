# Merge Orders with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/merge`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Merge Orders](https://api-docs.starshipit.com/#589357dc-f95d-4ac6-a54f-0ddb7d84b1fc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parent_order_id` | body | `number` | no |
| `child_order_ids[]` | body | `array<number>` | no |
