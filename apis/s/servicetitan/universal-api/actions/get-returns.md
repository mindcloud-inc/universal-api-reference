# ServiceTitan: Get Returns



```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-returns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-returns?${params}`, {
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
| `modifiedOnOrAfter` | string | no | Returns modified on or after this UTC timestamp. |
| `syncStatuses` | string | no | Sync status collection filter: Pending, Posted, or Exported. Accepts multiple values in one string, delimited by `,`. |
| `active` | list<string> | no | Active-state filter: True, Any, or False. One of: `Any`, `False`, `True`. |
| `ids` | string | no | Return IDs to retrieve, up to 50. Accepts multiple values in one string, delimited by `,`. |
| `number` | string | no | Return number filter. |
| `referenceNumber` | string | no | Reference number filter. |
| `jobId` | number | no | Job ID filter. |
| `purchaseOrderId` | number | no | Purchase order ID filter. |
| `batchId` | number | no | Batch ID filter. |
| `vendorIds` | string | no | Vendor ID collection filter. Accepts multiple values in one string, delimited by `,`. |
| `businessUnitIds` | string | no | Business unit ID collection filter. Accepts multiple values in one string, delimited by `,`. |
| `inventoryLocationIds` | string | no | Inventory location ID collection filter. Accepts multiple values in one string, delimited by `,`. |
| `returnDateOnOrAfter` | string | no | Returns with a return date on or after this timestamp. |
| `returnDateBefore` | string | no | Returns with a return date before this timestamp. |
| `createdOnOrAfter` | string | no | Returns created on or after this UTC timestamp. |
| `createdBefore` | string | no | Returns created before this UTC timestamp. |
| `modifiedBefore` | string | no | Returns modified before this UTC timestamp. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields.Fields` | object | no | Custom-field name and value pairs to filter by. |
| `customFields.Operator` | list<string> | no | How custom-field filters are combined: And or Or. One of: `And`, `Or`. |
| `page` | number | no | Page number, starting from 1. |
| `pageSize` | number | no | Number of records per page; ServiceTitan defaults to 50. |
| `includeTotal` | boolean | no | Whether to include the total matching record count. |
| `sort` | list<string> | no | Sort by Id, CreatedOn, or ModifiedOn. Prefix with + for ascending or - for descending. One of: `+CreatedOn`, `+Id`, `+ModifiedOn`, `-CreatedOn`, `-Id`, `-ModifiedOn`. |
| `externalDataApplicationGuid` | string | no | Application GUID whose external data should be returned. |
| `externalDataKey` | string | no | External data key; requires External Data Values. |
| `externalDataValues` | string | no | External data values; requires External Data Key and accepts up to 50. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET inventory/v2/tenant/{{credentials.tenant}}/returns` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-returns.md) for the provider-specific parameters and requirements.

