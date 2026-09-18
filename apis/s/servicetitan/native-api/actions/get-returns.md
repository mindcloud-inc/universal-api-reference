# Get Returns with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `inventory/v2/tenant/{tenant}/returns`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Returns](https://developer.servicetitan.io/docs/apis/tenant-inventory-v2/endpoints/Returns_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifiedOnOrAfter` | query | `string` | no | Returns modified on or after this UTC timestamp. |
| `syncStatuses` | query | `string` | no | Sync status collection filter: Pending, Posted, or Exported. Send multiple values as a string separated by `,`. |
| `active` | query | `list<string>` | no | Active-state filter: True, Any, or False. Accepted values: `Any`, `False`, `True`. |
| `ids` | query | `string` | no | Return IDs to retrieve, up to 50. Send multiple values as a string separated by `,`. |
| `number` | query | `string` | no | Return number filter. |
| `referenceNumber` | query | `string` | no | Reference number filter. |
| `jobId` | query | `number` | no | Job ID filter. |
| `purchaseOrderId` | query | `number` | no | Purchase order ID filter. |
| `batchId` | query | `number` | no | Batch ID filter. |
| `vendorIds` | query | `string` | no | Vendor ID collection filter. Send multiple values as a string separated by `,`. |
| `businessUnitIds` | query | `string` | no | Business unit ID collection filter. Send multiple values as a string separated by `,`. |
| `inventoryLocationIds` | query | `string` | no | Inventory location ID collection filter. Send multiple values as a string separated by `,`. |
| `customFields.Fields` | query | `object` | no | Custom-field name and value pairs to filter by. |
| `customFields.Operator` | query | `list<string>` | no | How custom-field filters are combined: And or Or. Accepted values: `And`, `Or`. |
| `returnDateOnOrAfter` | query | `string` | no | Returns with a return date on or after this timestamp. |
| `returnDateBefore` | query | `string` | no | Returns with a return date before this timestamp. |
| `createdOnOrAfter` | query | `string` | no | Returns created on or after this UTC timestamp. |
| `createdBefore` | query | `string` | no | Returns created before this UTC timestamp. |
| `modifiedBefore` | query | `string` | no | Returns modified before this UTC timestamp. |
| `page` | query | `number` | no | Page number, starting from 1. |
| `pageSize` | query | `number` | no | Number of records per page; ServiceTitan defaults to 50. |
| `includeTotal` | query | `boolean` | no | Whether to include the total matching record count. |
| `sort` | query | `list<string>` | no | Sort by Id, CreatedOn, or ModifiedOn. Prefix with + for ascending or - for descending. Accepted values: `+CreatedOn`, `+Id`, `+ModifiedOn`, `-CreatedOn`, `-Id`, `-ModifiedOn`. |
| `externalDataApplicationGuid` | query | `string` | no | Application GUID whose external data should be returned. |
| `externalDataKey` | query | `string` | no | External data key; requires External Data Values. |
| `externalDataValues` | query | `string` | no | External data values; requires External Data Key and accepts up to 50. Send multiple values as a string separated by `,`. |
