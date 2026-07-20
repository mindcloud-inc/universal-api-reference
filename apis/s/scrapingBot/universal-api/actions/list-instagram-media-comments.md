# ScrapingBot: List Instagram Media Comments



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-media-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-media-comments?connectionId=$CONNECTION_ID&media_id=3874501047187694857" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "media_id": "3874501047187694857"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-instagram-media-comments?${params}`, {
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
| `count` | number | no | Number of comments to return. Default: `3`. |
| `media_id` | string | yes | Instagram media ID. Default: `3874501047187694857`. |

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

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-instagram-media-comments.md) for the provider-specific parameters and requirements.

