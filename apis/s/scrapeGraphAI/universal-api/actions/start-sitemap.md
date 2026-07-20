# ScrapeGraphAI: Start Sitemap

Starts a sitemap extraction job in ScrapeGraphAI.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-sitemap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteUrl": "https://scrapegraphai.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-sitemap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteUrl": "https://scrapegraphai.com/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteUrl` | string | yes | Website URL whose sitemap should be discovered and extracted. Example: `https://scrapegraphai.com/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | object | no | Optional custom HTTP headers to send with the request. Example: `[object Object]`. |
| `mock` | boolean | no | Return mock data instead of performing a live sitemap extraction. Default: `false`. |
| `stealth` | boolean | no | Enable stealth mode to bypass bot protection. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string",
      "urls": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string |  |
| `urls` | array<string> |  |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /sitemap` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-sitemap.md) for the provider-specific parameters and requirements.

