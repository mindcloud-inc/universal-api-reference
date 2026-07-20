# Cloudflare Browser Run: Create Crawl Job

Creates a crawl job in Cloudflare Browser Run.

```
POST https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/create-crawl-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudflare Browser Run `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/create-crawl-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudflareBrowserRun/latest/actions/create-crawl-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Starting URL for the crawl job. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `formats[]` | array<string> | no | Formats to return from the crawl: html, markdown, or json. |
| `depth` | number | no | Maximum number of levels deep the crawler will traverse from the starting URL. |
| `limit` | number | no | Maximum number of URLs to crawl. |
| `render` | boolean | no | Whether to render pages or fetch static content. True by default. |
| `options` | object | no | Crawler options for include/exclude patterns, subdomains, and external links. |
| `cacheTTL` | number | no | Cache TTL in seconds. Set 0 to disable cache. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloudflare Browser Run API, this operation is `POST /accounts/:accountId/browser-rendering/crawl` (base URL `https://api.cloudflare.com/client/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-crawl-job.md) for the provider-specific parameters and requirements.

