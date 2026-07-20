# ScrapFly: Get Crawl Contents

Retrieves crawl contents from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-contents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-contents?connectionId=$CONNECTION_ID&crawlerUuid=bf7282d8-818f-4a17-b3d7-a97a8f49ee65" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "crawlerUuid": "bf7282d8-818f-4a17-b3d7-a97a8f49ee65"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/get-crawl-contents?${params}`, {
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
| `format` | string | no | Content format to return, such as markdown or html. Example: `markdown`. |
| `url` | string | no | Optional specific crawled URL to retrieve instead of the whole crawl content set. Example: `https://web-scraping.dev/page`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contents": {},
      "links": {
        "crawledUrls": "https://example.com",
        "next": "https://example.com",
        "prev": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contents` | object | Map of crawled URLs to fetched content payloads. |
| `links.crawledUrls` | string | URL to the crawled URLs listing endpoint. |
| `links.next` | string | URL for the next page of crawl contents when present. |
| `links.prev` | string | URL for the previous page of crawl contents when present. |

## Native endpoint

Through the native ScrapFly API, this operation is `GET /crawl/:crawlerUuid/contents` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-contents.md) for the provider-specific parameters and requirements.

