# Webcrawler API: Create Crawl Job

Creates a website crawl job in Webcrawler API.

```
POST https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-crawl-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-crawl-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-crawl-job', {
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
| `url` | string | yes | Target website URL to crawl. |
| `scrape_type` | string | no | Output format for crawled content. |
| `items_limit` | number | no | Maximum number of items to return. |
| `max_depth` | number | no | Maximum crawl depth. |
| `respect_robots_txt` | boolean | no | Whether to respect robots.txt rules. |
| `allow_subdomains` | boolean | no | Whether to crawl subdomains. |
| `main_content_only` | boolean | no | Whether to limit extraction to main content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whitelist_regexp` | string | no | Only include URLs matching this regular expression. |
| `blacklist_regexp` | string | no | Exclude URLs matching this regular expression. |
| `webhook_url` | string | no | Webhook URL for job completion notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created crawl job identifier. |

## Native endpoint

Through the native Webcrawler API API, this operation is `POST /v1/crawl` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-crawl-job.md) for the provider-specific parameters and requirements.

