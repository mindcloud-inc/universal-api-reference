# RO App: List Order Statuses



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-statuses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-order-statuses?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "comment": "string",
      "group": {
        "name": "Ava Chen",
        "type": 1
      },
      "id": 1,
      "name": "Ava Chen",
      "status_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `comment` | string |  |
| `group` | object |  |
| `group.name` | string |  |
| `group.type` | number |  |
| `id` | number |  |
| `name` | string |  |
| `status_id` | number |  |

## Native endpoint

Through the native RO App API, this operation is `GET /orders/statuses` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-order-statuses.md) for the provider-specific parameters and requirements.

