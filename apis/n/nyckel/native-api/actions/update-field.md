# Update Field with Nyckel

Updates an existing field in Nyckel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/functions/:functionId/fields/:fieldId`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `fieldId` | path | `string` | yes | Nyckel field identifier. |
| `name` | body | `string` | no | Updated field name. |
| `type` | body | `string` | no | Updated field type. |
