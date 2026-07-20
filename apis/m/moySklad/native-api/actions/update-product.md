# Update product with MoySklad

Updates a product in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/product/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update product](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-towar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Product update payload. |
| `id` | path | `string` | yes | MoySklad product ID. |
