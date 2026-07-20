# Wooxy: List Events

Finds events in your Wooxy account.

```
GET https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wooxy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/list-events?${params}`, {
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
      "data": {
        "cost": {},
        "createdAt": "string",
        "description": "string",
        "id": "string",
        "isConversion": true,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "limit": 1,
      "offset": 1,
      "result": true,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.cost` | object |  |
| `data.createdAt` | string |  |
| `data.description` | string |  |
| `data.id` | string |  |
| `data.isConversion` | boolean |  |
| `data.name` | string |  |
| `data.updatedAt` | string |  |
| `limit` | number |  |
| `offset` | number |  |
| `result` | boolean |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Wooxy API, this operation is `POST v3/custom-event/find` (base URL `https://api.wooxy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

