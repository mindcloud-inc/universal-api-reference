# List entity images with MoySklad

Retrieves entity images from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/:id/images`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List entity images](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-izobrazheniiami-v-towarah-modifikaciiakh-i-komplektah)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad entity type. |
| `id` | path | `string` | yes | MoySklad entity ID. |
