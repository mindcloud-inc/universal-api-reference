# Humanitix: List Orders

Retrieves orders for an event from Humanitix.

```
GET https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Humanitix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/humanitix/latest/actions/list-orders?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        [
          "string"
        ]
      ],
      "page": 1,
      "pageSize": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders[]` | array<string> |  |
| `page` | number |  |
| `pageSize` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Humanitix API, this operation is `GET /events/:eventId/orders` (base URL `https://api.humanitix.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

