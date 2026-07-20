# ScrapFly: Start Crawl

Creates a new crawl job in ScrapFly.

```
POST https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/start-crawl
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/start-crawl" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://web-scraping.dev/products"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/start-crawl', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://web-scraping.dev/products"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maxDepth` | number | no | Maximum link depth from the starting URL. Example: `2`. |
| `pageLimit` | number | no | Maximum pages to crawl. Use 0 for unlimited within subscription limits. Example: `25`. |
| `url` | string | yes | Starting URL for the crawl. Example: `https://web-scraping.dev/products`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "crawlerUuid": "string",
      "env": "string",
      "links": {
        "status": "https://example.com"
      },
      "project": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `crawlerUuid` | string | Created crawler UUID. |
| `env` | string | ScrapFly environment. |
| `links.status` | string | URL to the crawler status endpoint. |
| `project` | string | ScrapFly project name. |
| `status` | string | Crawler status. |

## Native endpoint

Through the native ScrapFly API, this operation is `POST /crawl` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-crawl.md) for the provider-specific parameters and requirements.

