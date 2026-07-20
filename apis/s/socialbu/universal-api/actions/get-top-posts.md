# Socialbu: Get Top Posts

Retrieves top-performing posts from SocialBu insights.

```
GET https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-top-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-top-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/get-top-posts?${params}`, {
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
      "account": {},
      "content": "string",
      "id": 1,
      "items": [
        {}
      ],
      "metrics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `content` | string |  |
| `id` | number |  |
| `items` | array<object> |  |
| `metrics` | object |  |

## Native endpoint

Through the native Socialbu API, this operation is `GET /insights/posts/top_posts` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-top-posts.md) for the provider-specific parameters and requirements.

