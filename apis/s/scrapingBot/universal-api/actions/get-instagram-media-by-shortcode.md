# ScrapingBot: Get Instagram Media by Shortcode



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-media-by-shortcode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-media-by-shortcode?connectionId=$CONNECTION_ID&shortcode=DXE_iyngGUJ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shortcode": "DXE_iyngGUJ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/get-instagram-media-by-shortcode?${params}`, {
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
| `shortcode` | string | yes | Instagram media shortcode. Default: `DXE_iyngGUJ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "display_url": "https://example.com",
      "duration": "string",
      "id": "string",
      "is_video": true,
      "owner": {},
      "shortcode": "string",
      "statusCode": 1,
      "taken_at_timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `display_url` | string |  |
| `duration` | string |  |
| `id` | string |  |
| `is_video` | boolean |  |
| `owner` | object |  |
| `shortcode` | string |  |
| `statusCode` | number |  |
| `taken_at_timestamp` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instagram-media-by-shortcode.md) for the provider-specific parameters and requirements.

