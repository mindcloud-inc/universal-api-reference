# Get Field with NocoDB

Retrieves details for a field from NocoDB.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/meta/bases/:baseId/fields/:fieldId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Get Field](https://nocodb.com/apis/v3/meta)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `fieldId` | path | `string` | yes | Field identifier. |
