# Update service with MoySklad

Updates a service in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/service/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update service](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-usluga)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Service update payload. |
| `id` | path | `string` | yes | MoySklad service ID. |
