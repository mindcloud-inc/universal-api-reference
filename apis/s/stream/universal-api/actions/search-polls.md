# Stream: Search Polls

Finds polls in Stream by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-polls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-polls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-polls?${params}`, {
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
| `filter` | object | no | Poll query filter object. |
| `limit` | number | no | Maximum number of polls to return. |
| `userId` | string | no | User ID query context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "polls": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |
| `polls` | array<object> |  |

## Native endpoint

Through the native Stream API, this operation is `POST /polls/query` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-polls.md) for the provider-specific parameters and requirements.

