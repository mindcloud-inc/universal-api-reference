# ServiceTitan: List AP Bills

Lists AP bills with line items and accounting details. Filter by bill type, sync status, and creation or modification dates.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-ap-bills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-ap-bills?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-ap-bills?${params}`, {
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
| `ids` | string | no | Comma-separated list of specific AP bill IDs to retrieve Accepts multiple values in one string, delimited by `,`. |
| `batchId` | number | no | Filter by specific batch ID |
| `batchNumber` | number | no | Filter by batch number |
| `billNumber` | string | no | Filter by bill number (partial match supported) |
| `businessUnitIds` | string | no | Comma-separated list of business unit IDs to filter by Accepts multiple values in one string, delimited by `,`. |
| `customField` | object | no |  |
| `customField.fields` | object | no | Dictionary of name-value pairs |
| `customField.operator` | list<string> | no | Operator to be used between the name-value pairs. Can be "Or" or "And", default is "And". Values: [And, Or] One of: `And`, `Or`. |
| `dateFrom` | date | no | Filter bills created on or after this date |
| `dateTo` | date | no | Filter bills created on or before this date |
| `jobNumber` | string | no | Filter by job number (partial match supported) |
| `purchaseOrderNumber` | string | no | Filter by purchase order number (partial match supported) |
| `purchaseOrderTypes` | string | no | Comma-separated list of purchase order types to filter by Accepts multiple values in one string, delimited by `,`. |
| `syncStatuses` | list<string> | no | Filter by sync status values One of: `Exported`, `Pending`, `Posted`, `PostedAndExported`. Accepts multiple values as an array. |
| `statuses` | list<string> | no | Filter by bill status values One of: `Canceled`, `Discrepancy`, `Reconciled`, `Unreconciled`. Accepts multiple values as an array. |
| `sources` | list<string> | no | Filter by bill source values One of: `API`, `OCR`, `Purchasing`, `Recurring`, `Standalone`, `Undefined`. Accepts multiple values as an array. |
| `minCost` | number | no | Filter bills with cost greater than or equal to this amount |
| `maxCost` | number | no | Filter bills with cost less than or equal to this amount |
| `billType` | list<string> | no | Filter by bill type (defaults to Procurement). Values: [NotSet, Procurement, ApBill] One of: `ApBill`, `NotSet`, `Procurement`. |
| `createdBefore` | date | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | date | no | Return items created on or after certain date/time (in UTC) |
| `modifiedBefore` | date | no | Return items modified before certain date/time (in UTC) |
| `modifiedOnOrAfter` | date | no | Return items modified on or after certain date/time (in UTC) |
| `dateReconciledBefore` | date | no | Filter by bills reconciled on or before this date |
| `dateReconciledOnOrAfter` | date | no | Filter by bills reconciled after this date |
| `threeWayMatchDiscrepancy` | list<string> | no | Filter by three-way match discrepancy status. Values: [NoDiscrepancy, Discrepancy] One of: `Discrepancy`, `NoDiscrepancy`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeTotal` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET accounting/v2/tenant/{{credentials.tenant}}/ap-bills` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ap-bills.md) for the provider-specific parameters and requirements.

