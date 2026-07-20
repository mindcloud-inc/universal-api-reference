# Update entity attribute with MoySklad

Updates an entity attribute in MoySklad.

## Endpoint

- **Method:** `PUT`
- **Path:** `entity/:entityType/metadata/attributes/:attributeId`
- **Base URL:** `https://api.moysklad.ru/api/remap/1.2`
- **Official documentation:** [Update entity attribute](https://dev.moysklad.ru/doc/api/remap/1.2/workbook/#workbook-rabota-s-dopolnitelnymi-poliami-cherez-json-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributeId` | path | `string` | yes | MoySklad attribute ID. |
| `body` | body | `object` | yes | Attribute update payload. |
| `entityType` | path | `string` | yes | MoySklad entity type. |
