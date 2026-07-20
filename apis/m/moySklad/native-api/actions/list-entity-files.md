# List entity files with MoySklad

Retrieves entity files from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/:id/files`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List entity files](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-failami-v-dokumentah-nomenklature-i-kontragentah)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad entity type. |
| `id` | path | `string` | yes | MoySklad entity ID. |
