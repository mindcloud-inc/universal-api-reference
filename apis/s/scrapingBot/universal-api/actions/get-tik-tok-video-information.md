# ScrapingBot: Get TikTok Video Information



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-tik-tok-video-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-tik-tok-video-information?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.tiktok.com%2F%40scout2015%2Fvideo%2F6718335390845095173" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.tiktok.com/@scout2015/video/6718335390845095173"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-tik-tok-video-information?${params}`, {
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
| `url` | string | yes | Full TikTok video URL. Default: `https://www.tiktok.com/@tiktok/video/7015738976982027525`. Example: `https://www.tiktok.com/@scout2015/video/6718335390845095173`. |
| `hd` | number | no | Set to 1 for HD download links. Default: `0`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "data": {},
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
| `creditsUsed` | number |  |
| `data` | object |  |
| `duration` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /tiktok` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-video-information.md) for the provider-specific parameters and requirements.

