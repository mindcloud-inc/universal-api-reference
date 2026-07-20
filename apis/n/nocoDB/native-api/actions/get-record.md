# Get Record with NocoDB

Retrieves a single record from a NocoDB table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/data/:baseId/:tableId/records/:recordId`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Get Record](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `tableId` | path | `string` | yes | Table identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
| `fields` | query | `string` | no | Comma-separated field names to include. |
| `linksAsLtar` | query | `boolean` | no | Whether to return linked records as Link To Another Record values. |
