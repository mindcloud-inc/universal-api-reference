# Scrapeless: Get Batch Scrape Job Status

Retrieves a batch scrape job status from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-batch-scrape-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-batch-scrape-job-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-batch-scrape-job-status?${params}`, {
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
      "completed": 1,
      "data": {
        "html": "string",
        "links": [
          "https://example.com"
        ],
        "markdown": "string",
        "metadata": {
          "<any other metadata>": "string",
          "description": "string",
          "error": "string",
          "language": "string",
          "sourceURL": "https://example.com",
          "statusCode": 1,
          "title": "string"
        },
        "rawHtml": "string",
        "screenshot": "string"
      },
      "status": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed` | number | The number of pages that have been successfully scraped. |
| `data` | array<object> | The data of the batch scrape. |
| `data.html` | string | HTML version of the content on page if `includeHtml`  is true |
| `data.links` | array<string> | List of links on the page if `includeLinks` is true |
| `data.markdown` | string |  |
| `data.metadata` | object |  |
| `data.metadata.<any other metadata>` | string |  |
| `data.metadata.description` | string |  |
| `data.metadata.error` | string | The error message of the page |
| `data.metadata.language` | string |  |
| `data.metadata.sourceURL` | string |  |
| `data.metadata.statusCode` | number | The status code of the page |
| `data.metadata.title` | string |  |
| `data.rawHtml` | string | Raw HTML content of the page if `includeRawHtml`  is true |
| `data.screenshot` | string | Screenshot of the page if `includeScreenshot` is true |
| `status` | string | The current status of the batch scrape. Can be `scraping`, `completed`, or `failed`. |
| `total` | number | The total number of pages that were attempted to be scraped. |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v1/crawler/scrape/batch/:id` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-batch-scrape-job-status.md) for the provider-specific parameters and requirements.

