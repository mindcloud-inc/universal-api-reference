# Webcrawler API: Create Scrape Job

Creates a single-page scrape job in Webcrawler API.

```
POST https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-scrape-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-scrape-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-scrape-job', {
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
| `url` | string | yes | Target page URL to scrape. |
| `include_links` | boolean | no | Include discovered links in the scrape result. |
| `output_format` | string | no | Requested scrape output format. Default: `markdown`. |
| `main_content_only` | boolean | no | Whether to focus extraction on the page's main content. |
| `respect_robots_txt` | boolean | no | Whether to respect robots.txt rules. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | no | Optional extraction prompt for the scrape. |
| `clean_selectors` | string | no | Selectors to remove before returning cleaned content. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Webcrawler API API returns.

## Native endpoint

Through the native Webcrawler API API, this operation is `POST /v2/scrape` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scrape-job.md) for the provider-specific parameters and requirements.

