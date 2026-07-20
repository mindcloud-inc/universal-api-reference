# Update Table Records with NocoDB

Updates records in a NocoDB table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v3/data/:baseId/:tableId/records`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Update Table Records](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `id` | body | `string` | yes | Record identifier. |
| `fields` | body | `object` | yes | Record field values to update. |
