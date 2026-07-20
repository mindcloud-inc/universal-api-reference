# Scrapeless: Get Crawl Job Errors

Retrieves crawl job errors from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-crawl-job-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-crawl-job-errors?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-crawl-job-errors?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": {
        "error": "string",
        "id": "string",
        "timestamp": "string",
        "url": "https://example.com"
      },
      "robotsBlocked": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Errored scrape jobs and error details |
| `errors.error` | string | Error message |
| `errors.id` | string |  |
| `errors.timestamp` | string | ISO timestamp of failure |
| `errors.url` | string | Scraped URL |
| `robotsBlocked` | array<string> | List of URLs that were attempted in scraping but were blocked by robots.txt |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v1/crawler/crawl/:id/errors` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-job-errors.md) for the provider-specific parameters and requirements.

