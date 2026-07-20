# WebinarGeek: List Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebinarGeek `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webinarGeek/latest/actions/list-subscriptions?${params}`, {
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
      "confirmationLink": "https://example.com",
      "createdAt": 1,
      "eligibleToWatch": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstname": "Ava",
      "id": 1,
      "unsubscribed": true,
      "watchLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmationLink` | string |  |
| `createdAt` | number |  |
| `eligibleToWatch` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstname` | string |  |
| `id` | number |  |
| `unsubscribed` | boolean |  |
| `watchLink` | string |  |

## Native endpoint

Through the native WebinarGeek API, this operation is `GET /subscriptions` (base URL `https://app.webinargeek.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

