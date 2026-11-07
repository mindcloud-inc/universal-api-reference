# Get Journal Entries with ServiceTitan

Gets a list of journal entries.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/journal-entries`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Journal Entries](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/JournalEntries_GetList)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postedFrom` | query | `date` | no | Posted on or after this date (time is ignored). |
| `postedTo` | query | `date` | no | Posted on or before this date (time is ignored). |
| `syncStatuses` | query | `list<string>` | no | Accepted values: `Error`, `Excluded`, `InProgress`, `NotSynced`, `OutOfSync`, `Synced`. Send multiple values as a string separated by `,`. |
| `statuses` | query | `list<string>` | no | Posting status of the journal entry. Accepted values: `Closed`, `Open`. Send multiple values as a string separated by `,`. |
| `transactionTypes` | query | `list<string>` | no | Returns journal entries that contain at least one transaction of these types. Accepted values: `BankDeposit`, `Bill`, `CostPoolAllocation`, `CreditMemo`, `CreditMemoApplication`, `Estimate`, `ExpenseTransaction`, `External`, `GrossPayItem`, `InventoryAdjustment`, `InventoryReturn`, `InventoryTransfer`, `Invoice`, `ItemConsumption`, `Manual`, `Payment`, `PaymentApplication`, `PayrollPeriod`, `PurchaseOrder`, `Receipt`, `RevenueRecognition`, `ServiceAgreementBudget`, `ServiceAgreementVisit`, `Subcontract`, `Unspecified`, `VendorCredit`, `VendorPayment`. Send multiple values as a string separated by `,`. |
| `empty` | query | `list<string>` | no | Whether empty journal entries are included. Has no effect when requesting by IDs. Accepted values: `Exclude`, `Include`, `IncludeExceptNotSynced`. |
| `businessUnitIds` | query | `list<number>` | no | Maximum 50 business units. Send multiple values as a string separated by `,`. |
| `transactionPostedFrom` | query | `date` | no | Contains a transaction posted on or after this date (time is ignored). |
| `transactionPostedTo` | query | `date` | no | Contains a transaction posted on or before this date (time is ignored). |
| `exportedFrom` | query | `date` | no | Exported on or after this date and time (UTC). |
| `exportedTo` | query | `date` | no | Exported on or before this date and time (UTC). |
| `exportedBy` | query | `string` | no | Comma-delimited list of user IDs, maximum 50. Send multiple values as a string separated by `,`. |
| `createdOnOrAfter` | query | `date` | no | — |
| `createdBefore` | query | `date` | no | — |
| `modifiedOnOrAfter` | query | `date` | no | — |
| `modifiedBefore` | query | `date` | no | — |
| `numberFrom` | query | `number` | no | Journal entry number is greater than or equal to this value. |
| `numberTo` | query | `number` | no | Journal entry number is less than or equal to this value. |
| `name` | query | `string` | no | Journal entry name contains this text. |
| `refNumber` | query | `string` | no | Comma-delimited list of reference numbers, maximum 50. Send multiple values as a string separated by `,`. |
| `customerName` | query | `string` | no | Contains a transaction for a customer whose name contains this text. |
| `locationName` | query | `string` | no | Contains a transaction for a customer location whose name contains this text. |
| `vendorName` | query | `string` | no | Contains a transaction for a vendor whose name contains this text. |
| `inventoryLocationName` | query | `string` | no | Contains a transaction for an inventory location whose name contains this text. |
| `ids` | query | `string` | no | Comma-delimited list of journal entry IDs, maximum 50 items Send multiple values as a string separated by `,`. |
| `serviceAgreementIds` | query | `string` | no | Comma-delimited list of service agreement IDs, maximum 50. Send multiple values as a string separated by `,`. |
