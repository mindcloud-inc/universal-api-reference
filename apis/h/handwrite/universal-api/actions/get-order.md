# Handwrite: Get Order

Retrieves an order from Handwrite.

```
GET https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Handwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/handwrite/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | The Handwrite order ID returned by the send endpoint or visible in the Handwrite app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "card": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "environment": "string",
      "from": {},
      "handwriting": "string",
      "message": "string",
      "meta": {},
      "origin": "string",
      "proofs": [
        {}
      ],
      "status": "string",
      "to": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Handwrite order ID. |
| `card` | string | Selected stationery ID. |
| `createdAt` | date | Order creation timestamp. |
| `environment` | string | Handwrite environment for the order. |
| `from` | object | Sender object stored on the order. |
| `handwriting` | string | Selected handwriting ID. |
| `message` | string | Letter message text. |
| `meta` | object | Additional metadata returned by Handwrite. |
| `origin` | string | Order creation origin. |
| `proofs` | array<object> | Proof image records when available. |
| `status` | string | Order status such as processing, written, complete, problem, or cancelled. |
| `to` | object | Recipient object stored on the order. |

## Native endpoint

Through the native Handwrite API, this operation is `GET /order/:orderId` (base URL `https://api.handwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

