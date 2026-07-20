# Humanitix: Get Order

Retrieves an order for an event from Humanitix.

```
GET https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humanitix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-order?connectionId=$CONNECTION_ID&eventId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/get-order?${params}`, {
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
| `eventId` | string | yes | The Humanitix event ID. |
| `orderId` | string | yes | The Humanitix order ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Humanitix API returns.

## Native endpoint

Through the native Humanitix API, this operation is `GET /events/:eventId/orders/:orderId` (base URL `https://api.humanitix.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

