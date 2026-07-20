# List Table Records with NocoDB

Retrieves records from a NocoDB table.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v3/data/:baseId/:tableId/records`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [List Table Records](https://nocodb.com/apis/v3/data)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base ID for the NocoDB base. |
| `tableId` | path | `string` | yes | Table ID for the NocoDB table. |
| `fields` | query | `string` | no | Comma-separated field names to include from linked records. |
| `viewId` | query | `string` | no | Only return records visible in the specified view. |
| `linksAsLtar` | query | `boolean` | no | Return linked record data instead of counts for link fields. |
