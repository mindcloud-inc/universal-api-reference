# List AP Bills with ServiceTitan

Lists AP bills with line items and accounting details. Filter by bill type, sync status, and creation or modification dates.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/ap-bills`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [List AP Bills](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApBills_GetListPaginated)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-separated list of specific AP bill IDs to retrieve Send multiple values as a string separated by `,`. |
| `batchId` | query | `number` | no | Filter by specific batch ID |
| `batchNumber` | query | `number` | no | Filter by batch number |
| `billNumber` | query | `string` | no | Filter by bill number (partial match supported) |
| `businessUnitIds` | query | `string` | no | Comma-separated list of business unit IDs to filter by Send multiple values as a string separated by `,`. |
| `customField` | query | `object` | no | — |
| `customField.Fields` | query | `object` | no | Dictionary of name-value pairs |
| `customField.Operator` | query | `list<string>` | no | Operator to be used between the name-value pairs. Can be "Or" or "And", default is "And". Values: [And, Or] Accepted values: `And`, `Or`. |
| `dateFrom` | query | `date` | no | Filter bills created on or after this date |
| `dateTo` | query | `date` | no | Filter bills created on or before this date |
| `jobNumber` | query | `string` | no | Filter by job number (partial match supported) |
| `purchaseOrderNumber` | query | `string` | no | Filter by purchase order number (partial match supported) |
| `purchaseOrderTypes` | query | `string` | no | Comma-separated list of purchase order types to filter by Send multiple values as a string separated by `,`. |
| `syncStatuses` | query | `list<string>` | no | Filter by sync status values Accepted values: `Exported`, `Pending`, `Posted`, `PostedAndExported`. Send multiple values as a array. |
| `statuses` | query | `list<string>` | no | Filter by bill status values Accepted values: `Canceled`, `Discrepancy`, `Reconciled`, `Unreconciled`. Send multiple values as a array. |
| `sources` | query | `list<string>` | no | Filter by bill source values Accepted values: `API`, `OCR`, `Purchasing`, `Recurring`, `Standalone`, `Undefined`. Send multiple values as a array. |
| `minCost` | query | `number` | no | Filter bills with cost greater than or equal to this amount |
| `maxCost` | query | `number` | no | Filter bills with cost less than or equal to this amount |
| `billType` | query | `list<string>` | no | Filter by bill type (defaults to Procurement). Values: [NotSet, Procurement, ApBill] Accepted values: `ApBill`, `NotSet`, `Procurement`. |
| `createdBefore` | query | `date` | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | query | `date` | no | Return items created on or after certain date/time (in UTC) |
| `modifiedBefore` | query | `date` | no | Return items modified before certain date/time (in UTC) |
| `modifiedOnOrAfter` | query | `date` | no | Return items modified on or after certain date/time (in UTC) |
| `dateReconciledBefore` | query | `date` | no | Filter by bills reconciled on or before this date |
| `dateReconciledOnOrAfter` | query | `date` | no | Filter by bills reconciled after this date |
| `includeTotal` | query | `boolean` | no | — |
| `threeWayMatchDiscrepancy` | query | `list<string>` | no | Filter by three-way match discrepancy status. Values: [NoDiscrepancy, Discrepancy] Accepted values: `Discrepancy`, `NoDiscrepancy`. |
