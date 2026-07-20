# Update Field with NocoDB

Updates details for a field in NocoDB.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/meta/bases/:baseId/fields/:fieldId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Update Field](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `fieldId` | path | `string` | yes | Field identifier. |
| `title` | body | `string` | no | Title of the field. |
| `type` | body | `string` | no | Field data type. |
| `description` | body | `string` | no | Description of the field. |
| `unique` | body | `boolean` | no | Whether the field should enforce unique values. |
| `options` | body | `object` | no | Field-type-specific options. |
