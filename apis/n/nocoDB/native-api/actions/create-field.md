# Create Field with NocoDB

Creates a new field in a NocoDB table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/meta/bases/:baseId/tables/:tableId/fields`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Create Field](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `title` | body | `string` | yes | Title of the field. |
| `type` | body | `string` | yes | Field data type. |
| `description` | body | `string` | no | Description of the field. |
| `unique` | body | `boolean` | no | Whether the field should enforce unique values. |
| `options` | body | `object` | no | Field-type-specific options. |
