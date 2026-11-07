# ServiceTitan: Get Journal Entries

Gets a list of journal entries.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-journal-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-journal-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-journal-entries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `postedFrom` | date | no | Posted on or after this date (time is ignored). Example: `2026-10-01`. |
| `postedTo` | date | no | Posted on or before this date (time is ignored). Example: `2026-10-31`. |
| `syncStatuses` | list<string> | no | One of: `Error`, `Excluded`, `InProgress`, `NotSynced`, `OutOfSync`, `Synced`. Accepts multiple values in one string, delimited by `,`. |
| `statuses` | list<string> | no | Posting status of the journal entry. One of: `Closed`, `Open`. Accepts multiple values in one string, delimited by `,`. |
| `transactionTypes` | list<string> | no | Returns journal entries that contain at least one transaction of these types. One of: `BankDeposit`, `Bill`, `CostPoolAllocation`, `CreditMemo`, `CreditMemoApplication`, `Estimate`, `ExpenseTransaction`, `External`, `GrossPayItem`, `InventoryAdjustment`, `InventoryReturn`, `InventoryTransfer`, `Invoice`, `ItemConsumption`, `Manual`, `Payment`, `PaymentApplication`, `PayrollPeriod`, `PurchaseOrder`, `Receipt`, `RevenueRecognition`, `ServiceAgreementBudget`, `ServiceAgreementVisit`, `Subcontract`, `Unspecified`, `VendorCredit`, `VendorPayment`. Accepts multiple values in one string, delimited by `,`. |
| `empty` | list<string> | no | Whether empty journal entries are included. Has no effect when requesting by IDs. One of: `Exclude`, `Include`, `IncludeExceptNotSynced`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessUnitIds` | list<number> | no | Maximum 50 business units. Accepts multiple values in one string, delimited by `,`. |
| `transactionPostedFrom` | date | no | Contains a transaction posted on or after this date (time is ignored). |
| `transactionPostedTo` | date | no | Contains a transaction posted on or before this date (time is ignored). |
| `exportedFrom` | date | no | Exported on or after this date and time (UTC). |
| `exportedTo` | date | no | Exported on or before this date and time (UTC). |
| `exportedBy` | string | no | Comma-delimited list of user IDs, maximum 50. Accepts multiple values in one string, delimited by `,`. |
| `createdOnOrAfter` | date | no |  |
| `createdBefore` | date | no |  |
| `modifiedOnOrAfter` | date | no |  |
| `modifiedBefore` | date | no |  |
| `numberFrom` | number | no | Journal entry number is greater than or equal to this value. |
| `numberTo` | number | no | Journal entry number is less than or equal to this value. |
| `name` | string | no | Journal entry name contains this text. |
| `refNumber` | string | no | Comma-delimited list of reference numbers, maximum 50. Accepts multiple values in one string, delimited by `,`. |
| `customerName` | string | no | Contains a transaction for a customer whose name contains this text. |
| `locationName` | string | no | Contains a transaction for a customer location whose name contains this text. |
| `vendorName` | string | no | Contains a transaction for a vendor whose name contains this text. |
| `inventoryLocationName` | string | no | Contains a transaction for an inventory location whose name contains this text. |
| `ids` | string | no | Comma-delimited list of journal entry IDs, maximum 50 items Accepts multiple values in one string, delimited by `,`. |
| `serviceAgreementIds` | string | no | Comma-delimited list of service agreement IDs, maximum 50. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/journal-entries` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-journal-entries.md) for the provider-specific parameters and requirements.

