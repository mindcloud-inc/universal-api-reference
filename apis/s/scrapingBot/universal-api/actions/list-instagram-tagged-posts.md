# ScrapingBot: List Instagram Tagged Posts



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-tagged-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-tagged-posts?connectionId=$CONNECTION_ID&user_id=25025320" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "user_id": "25025320"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-tagged-posts?${params}`, {
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
| `count` | number | no | Number of tagged posts to return. Default: `3`. |
| `user_id` | string | yes | Instagram user ID. Default: `25025320`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "creditsUsed": 1,
      "duration": "string",
      "edges": [
        {}
      ],
      "page_info": {},
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `creditsUsed` | number |  |
| `duration` | string |  |
| `edges` | array<object> |  |
| `page_info` | object |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instagram-tagged-posts.md) for the provider-specific parameters and requirements.

