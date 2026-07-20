# Ecwid: Get Order

Retrieves an order from Ecwid.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-order?${params}`, {
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
| `orderId` | number | yes | Ecwid order ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecwid API returns.

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/orders/:orderId` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

