# Create Table Records with NocoDB

Creates new records in a NocoDB table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/data/:baseId/:tableId/records`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Create Table Records](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `fields` | body | `object` | yes | Record field values for the new record. |
