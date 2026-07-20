# Shipday: Search Delivery Orders

Finds delivery orders in Shipday by query filters.

```
GET https://connect.mindcloud.co/v1/universal/shipday/latest/actions/search-delivery-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/search-delivery-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/search-delivery-orders?${params}`, {
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
| `startTime` | date | no | Start timestamp for the delivery-order query window. Example: `2020-01-01T00:00:00Z`. |
| `endTime` | date | no | End timestamp for the delivery-order query window. Example: `2021-04-11T23:59:59Z`. |
| `orderStatus` | string | no | Order-status filter applied to the query. Example: `ALREADY_DELIVERED`. |
| `startCursor` | number | no | Start cursor for the returned order range. Example: `1`. |
| `endCursor` | number | no | End cursor for the returned order range. Example: `3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shipday API returns.

## Native endpoint

Through the native Shipday API, this operation is `POST /orders/query` (base URL `https://api.shipday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-delivery-orders.md) for the provider-specific parameters and requirements.

