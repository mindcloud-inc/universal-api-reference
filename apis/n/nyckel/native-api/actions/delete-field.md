# Delete Field with Nyckel

Deletes an existing field from Nyckel.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/functions/:functionId/fields/:fieldId`
- **Base URL:** `https://www.nyckel.com/v1`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Nyckel function identifier. |
| `fieldId` | path | `string` | yes | Nyckel field identifier. |
