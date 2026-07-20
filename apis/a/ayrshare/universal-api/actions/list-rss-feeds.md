# Ayrshare: List RSS Feeds

Retrieves RSS feeds from Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-rss-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-rss-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/list-rss-feeds?${params}`, {
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
      "code": 1,
      "feeds": [
        {}
      ],
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `feeds` | array<object> | Registered RSS feeds. |
| `message` | string | Feed or error message. |
| `status` | string | Feed list status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /feed` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-rss-feeds.md) for the provider-specific parameters and requirements.

