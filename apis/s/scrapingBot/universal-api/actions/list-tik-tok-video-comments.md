# ScrapingBot: List TikTok Video Comments



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-video-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-video-comments?connectionId=$CONNECTION_ID&aweme_id=7191482515322776874" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aweme_id": "7191482515322776874"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-video-comments?${params}`, {
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
| `aweme_id` | string | yes | TikTok video ID. Default: `7015738976982027525`. Example: `7191482515322776874`. |
| `count` | number | no | Number of comments to return. Default: `3`. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "creditsUsed": 1,
      "duration": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `creditsUsed` | number |  |
| `duration` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /tiktok` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tik-tok-video-comments.md) for the provider-specific parameters and requirements.

