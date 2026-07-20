# ScrapFly: Batch Crawl Contents

Retrieves batched crawl contents from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/batch-crawl-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/batch-crawl-contents?connectionId=$CONNECTION_ID&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65&urls=https%3A%2F%2Fweb-scraping.dev%2Fpage1%0Ahttps%3A%2F%2Fweb-scraping.dev%2Fpage2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerUuid": "bf7282d8-818f-4a17-b3d7-a97a8f49ee65",
  "urls": "https://web-scraping.dev/page1\nhttps://web-scraping.dev/page2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/batch-crawl-contents?${params}`, {
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
| `crawlerUuid` | string | yes | Crawler job identifier returned when a crawl starts. Example: `bf7282d8-818f-4a17-b3d7-a97a8f49ee65`. |
| `formats` | string | no | Comma-separated list of output formats to retrieve, such as markdown,text. Example: `markdown,text`. |
| `urls` | string | yes | Plain-text list of URLs to retrieve, separated by spaces or new lines. Example: `https://web-scraping.dev/page1 https://web-scraping.dev/page2`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ScrapFly API returns.

## Native endpoint

Through the native ScrapFly API, this operation is `POST /crawl/:crawlerUuid/contents/batch` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-crawl-contents.md) for the provider-specific parameters and requirements.

