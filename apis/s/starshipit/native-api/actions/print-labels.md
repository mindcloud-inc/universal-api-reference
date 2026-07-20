# Print Labels with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/shipments`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Print Labels](https://api-docs.starshipit.com/#21741468-85a4-4dbb-b11c-1fe582fd54ce)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_ids[]` | body | `array<number>` | no |
| `reprint` | body | `boolean` | no |
