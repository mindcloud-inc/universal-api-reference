# Scrape Creators: Get TikTok Trending Feed

Retrieves TikTok trending feed items from Scrape Creators.

```
GET https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-trending-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape Creators `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-trending-feed?connectionId=$CONNECTION_ID&region=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "region": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeCreators/latest/actions/get-tik-tok-trending-feed?${params}`, {
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
| `region` | string | yes | Region code |
| `trim` | boolean | no | Return a trimmed response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aweme_list": [
        {}
      ],
      "credits_remaining": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aweme_list` | array<object> |  |
| `credits_remaining` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Scrape Creators API, this operation is `GET /v1/tiktok/get-trending-feed` (base URL `https://api.scrapecreators.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tik-tok-trending-feed.md) for the provider-specific parameters and requirements.

