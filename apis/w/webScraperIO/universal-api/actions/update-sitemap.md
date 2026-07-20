# WebScraper.IO: Update Sitemap

Updates an existing sitemap in WebScraper.IO.

```
PUT https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/update-sitemap
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraper.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/update-sitemap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "selectors[]": [
    {}
  ],
  "sitemapId": 1,
  "sitemapKey": "string",
  "startUrls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webScraperIO/latest/actions/update-sitemap', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "selectors[]": [{}],
    "sitemapId": 1,
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
| `sitemapId` | number | yes | The Web Scraper sitemap ID. |
| `sitemapKey` | string | yes | The sitemap key used by Web Scraper. |
| `startUrls[]` | array<string> | yes | The start URLs for the sitemap. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string | Update result string. |

## Native endpoint

Through the native WebScraper.IO API, this operation is `PUT /sitemap/:sitemapId` (base URL `https://api.webscraper.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sitemap.md) for the provider-specific parameters and requirements.

