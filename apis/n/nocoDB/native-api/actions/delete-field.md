# Delete Field with NocoDB

Deletes an existing field from NocoDB.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v3/meta/bases/:baseId/fields/:fieldId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Delete Field](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `fieldId` | path | `string` | yes | Field identifier. |
