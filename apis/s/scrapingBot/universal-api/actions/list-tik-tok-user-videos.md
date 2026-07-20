# ScrapingBot: List TikTok User Videos



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-user-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-user-videos?connectionId=$CONNECTION_ID&unique_id=tiktok" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "unique_id": "tiktok"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/list-tik-tok-user-videos?${params}`, {
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
| `unique_id` | string | yes | TikTok username without @. Default: `tiktok`. Example: `tiktok`. |
| `count` | number | no | Number of videos to return. Default: `3`. Example: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "duration": "string",
      "items": [
        {}
      ],
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `duration` | string |  |
| `items` | array<object> |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /tiktok` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tik-tok-user-videos.md) for the provider-specific parameters and requirements.

