# Explara: Event Cart Calculation

Retrieves an event cart calculation from Explara.

```
GET https://connect.mindcloud.co/v1/universal/explara/latest/actions/event-cart-calculation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Explara `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/event-cart-calculation?connectionId=$CONNECTION_ID&eventId=string&tickets%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "tickets[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explara/latest/actions/event-cart-calculation?${params}`, {
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
| `eventId` | string | yes | Explara event identifier. |
| `tickets[]` | array<object> | yes | Array of ticket selection objects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Explara API returns.

## Native endpoint

Through the native Explara API, this operation is `POST /api/publisher/cart-calculation` (base URL `https://www.explara.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/event-cart-calculation.md) for the provider-specific parameters and requirements.

