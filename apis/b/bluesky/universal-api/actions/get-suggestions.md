# Bluesky: Get Suggestions

Retrieves suggested Bluesky accounts to follow.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggestions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/get-suggestions?${params}`, {
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
      "actors": [
        {}
      ],
      "cursor": "string",
      "recId": 1,
      "recIdStr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actors` | array<object> |  |
| `cursor` | string |  |
| `recId` | number |  |
| `recIdStr` | string |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.actor.getSuggestions` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-suggestions.md) for the provider-specific parameters and requirements.

