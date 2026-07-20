# Create entity attribute with MoySklad

Creates an entity attribute in MoySklad.

## Endpoint

- **Method:** `POST`
- **Path:** `entity/:entityType/metadata/attributes`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Create entity attribute](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | MoySklad entity type. |
| `name` | body | `string` | yes | MoySklad name argument. |
| `required` | body | `boolean` | no | MoySklad required argument. |
| `type` | body | `string` | yes | MoySklad type argument. |
