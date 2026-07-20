# Webcrawler API: Create Feed

Creates a scheduled website monitoring feed in Webcrawler API.

```
POST https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webcrawler API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/create-feed', {
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
| `url` | string | yes | Website URL to monitor. |
| `name` | string | no | Friendly feed name. |
| `scrape_type` | string | no | Content format for feed items. |
| `items_limit` | number | no | Maximum pages per crawl run. |
| `respect_robots_txt` | boolean | no | Whether to honor robots.txt. |
| `max_depth` | number | no | Maximum crawl depth. |
| `allow_subdomains` | boolean | no | Whether the feed may crawl subdomains. |
| `main_content_only` | boolean | no | Whether extraction should focus on main content only. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `whitelist_regexp` | string | no | Only include URLs matching this regular expression. |
| `blacklist_regexp` | string | no | Exclude URLs matching this regular expression. |
| `webhook_url` | string | no | Webhook URL for feed run notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "nextRunAt": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created feed identifier. |
| `nextRunAt` | string | Scheduled next run timestamp for the feed when returned. |
| `status` | string | Current feed status after creation. |
| `url` | string | Configured feed URL. |

## Native endpoint

Through the native Webcrawler API API, this operation is `POST /v2/feed` (base URL `https://api.webcrawlerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feed.md) for the provider-specific parameters and requirements.

