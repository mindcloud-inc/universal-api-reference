# Middesk: List agent threads

Retrieves agent threads from your Middesk account.

```
GET https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-agent-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Middesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-agent-threads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/middesk/latest/actions/list-agent-threads?${params}`, {
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
      "data": [
        {}
      ],
      "hasMore": true,
      "object": "string",
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
| `hasMore` | boolean |  |
| `object` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Middesk API, this operation is `GET /threads` (base URL `https://api.middesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agent-threads.md) for the provider-specific parameters and requirements.

