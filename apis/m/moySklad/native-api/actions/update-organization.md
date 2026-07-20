# Update organization with MoySklad

Updates an organization in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/organization/:id`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update organization](https://dev.moysklad.ru/doc/api/remap/1.2/dictionaries/#suschnosti-iurlico)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Organization update payload. |
| `id` | path | `string` | yes | MoySklad organization ID. |
