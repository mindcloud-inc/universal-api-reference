# List entity attributes with MoySklad

Retrieves entity attributes from MoySklad.

## Endpoint

- **Method:** `GET`
- **Path:** `entity/:entityType/metadata/attributes`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [List entity attributes](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad entity type. |
