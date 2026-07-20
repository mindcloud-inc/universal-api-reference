# Update store with MoySklad

Updates a store in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/store/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update store](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-sklad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Store update payload. |
| `id` | path | `string` | yes | MoySklad store ID. |
