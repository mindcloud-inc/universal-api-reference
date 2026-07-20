# Sympla: List Participants By Order

Retrieves participants from Sympla for a specific order.

```
GET https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-participants-by-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sympla `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-participants-by-order?connectionId=$CONNECTION_ID&eventId=string&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string",
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sympla/latest/actions/list-participants-by-order?${params}`, {
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
| `eventId` | string | yes | Unique identifier of the event. |
| `orderId` | string | yes | Unique identifier of the order within the event. |
| `fields` | string | no | Optional comma-separated response fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "pagination": {},
      "sort": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `pagination` | object |  |
| `sort` | object |  |

## Native endpoint

Through the native Sympla API, this operation is `GET /events/:eventId/orders/:orderId/participants` (base URL `https://api.sympla.com.br/public/v1.5.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-participants-by-order.md) for the provider-specific parameters and requirements.

