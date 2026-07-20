# ScrapFly: Scrape URL

Retrieves a scraped page from ScrapFly.

```
GET https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb-scraping.dev%2Fproduct%2F1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://web-scraping.dev/product/1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url?${params}`, {
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
| `url` | string | yes | Target URL to scrape. Example: `https://web-scraping.dev/product/1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {
        "method": "string",
        "project": "string",
        "url": "https://example.com"
      },
      "result": {
        "contentType": "string",
        "logUrl": "https://example.com",
        "statusCode": 1,
        "success": true,
        "url": "https://example.com"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config.method` | string | HTTP method used for the scrape request. |
| `config.project` | string | ScrapFly project name. |
| `config.url` | string | Requested target URL. |
| `result.contentType` | string | Returned content type. |
| `result.logUrl` | string | ScrapFly dashboard log URL. |
| `result.statusCode` | number | Upstream HTTP status code. |
| `result.success` | boolean | Whether the scrape completed successfully. |
| `result.url` | string | Resolved target URL. |
| `uuid` | string | Scrape run UUID. |

## Native endpoint

Through the native ScrapFly API, this operation is `GET /scrape` (base URL `https://api.scrapfly.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url.md) for the provider-specific parameters and requirements.

