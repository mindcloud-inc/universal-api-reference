# Amazon Vendor: List Direct Fulfillment Orders



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/list-direct-fulfillment-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/list-direct-fulfillment-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&createdAfter=2026-05-07T12%3A00%3A00.000Z&createdBefore=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "createdAfter": "2026-05-07T12:00:00.000Z",
  "createdBefore": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/list-direct-fulfillment-orders?${params}`, {
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
| `createdAfter` | date | yes | Purchase orders that became available after this ISO-8601 date/time. |
| `createdBefore` | date | yes | Purchase orders that became available before this ISO-8601 date/time. |
| `shipFromPartyId` | string | no | Vendor warehouse identifier for the fulfillment warehouse. |
| `status` | list | no | Purchase order status to return. One of: `Accepted`, `Cancelled`, `New`, `Shipped`. |
| `sortOrder` | list | no | Sort order by order creation date. One of: `Ascending`, `Descending`. |
| `includeDetails` | string | no | When true, returns complete purchase order details; otherwise only purchase order numbers. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/directFulfillment/orders/2021-12-28/purchaseOrders` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-direct-fulfillment-orders.md) for the provider-specific parameters and requirements.

