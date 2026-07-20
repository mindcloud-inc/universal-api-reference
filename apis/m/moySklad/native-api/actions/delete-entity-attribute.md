# Delete entity attribute with MoySklad

Deletes an entity attribute from MoySklad.

## Endpoint

- **Method:** `DELETE`
- **Path:** `entity/:entityType/metadata/attributes/:attributeId`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Delete entity attribute](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributeId` | path | `string` | yes | MoySklad attribute ID. |
| `entityType` | path | `string` | yes | MoySklad entity type. |
