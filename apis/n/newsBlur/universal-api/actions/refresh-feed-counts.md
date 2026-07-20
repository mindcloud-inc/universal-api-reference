# NewsBlur: Refresh Feed Counts

Retrieves unread feed counts from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/refresh-feed-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/refresh-feed-counts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/refresh-feed-counts?${params}`, {
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
      "authenticated": true,
      "feeds": {},
      "result": "string",
      "social_feeds": {},
      "starred_count": 1,
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `feeds` | object | Feed counts keyed by feed ID. |
| `result` | string | Result status. |
| `social_feeds` | object | Social feed counts keyed by ID. |
| `starred_count` | number | Total saved story count. |
| `user_id` | number | Authenticated NewsBlur user ID. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/refresh_feeds` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-feed-counts.md) for the provider-specific parameters and requirements.

