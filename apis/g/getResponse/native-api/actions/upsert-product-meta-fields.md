# Upsert Product Meta Fields with GetResponse

Creates or updates product meta fields for a GetResponse shop product.

## Endpoint

- **Method:** `POST`
- **Path:** `/shops/:shopId/products/:productId/meta-fields`
- **Base URL:** `https://api.getresponse.com/v3`
- **Official documentation:** [Upsert Product Meta Fields](https://apireference.getresponse.com/#operation/upsertMetaFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shopId` | path | `string` | yes | The shop ID |
| `productId` | path | `string` | yes | The product ID |
| `metaFields[]` | body | `array<object>` | yes | Meta fields to upsert |
| `metaFields[].metaFieldId` | body | `string` | yes | Meta field identifier |
