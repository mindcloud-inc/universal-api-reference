# Sender: List Subscribers



```
GET https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sender `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sender/latest/actions/list-subscribers?${params}`, {
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
      "bouncedAt": "2026-05-07T12:00:00.000Z",
      "columns": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "ipAddress": "string",
      "lastname": "Chen",
      "location": "string",
      "phone": "string",
      "phoneCountry": "string",
      "source": "string",
      "status": {},
      "subscriberTags": [
        {}
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bouncedAt` | date |  |
| `columns` | array<object> |  |
| `created` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `lastname` | string |  |
| `location` | string |  |
| `phone` | string |  |
| `phoneCountry` | string |  |
| `source` | string |  |
| `status` | object |  |
| `subscriberTags` | array<object> |  |
| `unsubscribedAt` | date |  |

## Native endpoint

Through the native Sender API, this operation is `GET /subscribers` (base URL `https://api.sender.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

