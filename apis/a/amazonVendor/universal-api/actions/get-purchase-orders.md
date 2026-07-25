# Amazon Vendor: Get Purchase Orders



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-orders?${params}`, {
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
| `createdAfter` | date | no | Purchase orders that became available after this ISO-8601 timestamp. |
| `createdBefore` | date | no | Purchase orders that became available before this ISO-8601 timestamp. |
| `changedAfter` | date | no | Purchase orders that changed after this ISO-8601 timestamp. |
| `changedBefore` | date | no | Purchase orders that changed before this ISO-8601 timestamp. |
| `sortOrder` | list | no | Sort ascending or descending by purchase order creation date. One of: `ASC`, `DESC`. |
| `includeDetails` | boolean | no | When true, returns purchase orders with complete details. Otherwise, only purchase order numbers are returned. |
| `poItemState` | list | no | Current state of the purchase order item. Amazon documents Cancelled as the allowed value. One of: `Cancelled`. |
| `isPOChanged` | boolean | no | When true, returns purchase orders modified after placement. |
| `purchaseOrderState` | list | no | Filters purchase orders by purchase order state. One of: `Acknowledged`, `Closed`, `New`. |
| `orderingVendorCode` | string | no | Filters purchase orders by ordering vendor code matching sellingParty.partyId. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/orders/v1/purchaseOrders` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-purchase-orders.md) for the provider-specific parameters and requirements.

