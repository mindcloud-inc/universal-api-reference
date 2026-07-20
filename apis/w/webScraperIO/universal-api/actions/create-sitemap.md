# WebScraper.IO: Create Sitemap

Creates a new sitemap in WebScraper.IO.

```
POST https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-sitemap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "selectors[]": [
    {}
  ],
  "sitemapKey": "string",
  "startUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/create-sitemap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "selectors[]": [{}],
    "sitemapKey": "string",
    "startUrls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `selectors[]` | array<object> | yes | The selector definitions for the sitemap. |
| `sitemapKey` | string | yes | The sitemap key used by Web Scraper. |
| `startUrls[]` | array<string> | yes | The start URLs for the sitemap. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created sitemap identifier. |

## Native endpoint

Through the native WebScraper.IO API, this operation is `POST /sitemap` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sitemap.md) for the provider-specific parameters and requirements.

