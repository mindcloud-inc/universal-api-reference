# World News API: Website to RSS Feed

Converts a website to an RSS feed using World News API.

```
GET https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/website-to-rss-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a World News API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/website-to-rss-feed?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fwww.cnn.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://www.cnn.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/website-to-rss-feed?${params}`, {
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
| `extractNews` | boolean | no | When true, extract full news details into the RSS output. |
| `url` | string | yes | Website URL to convert into an RSS feed. Default: `https://www.cnn.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "rss": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `rss` | string | Generated RSS feed content in XML format. |

## Native endpoint

Through the native World News API API, this operation is `GET /feed.rss` (base URL `https://api.worldnewsapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/website-to-rss-feed.md) for the provider-specific parameters and requirements.

