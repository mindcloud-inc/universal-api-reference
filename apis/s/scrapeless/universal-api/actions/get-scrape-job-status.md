# Scrapeless: Get Scrape Job Status

Retrieves a scrape job status from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scrape-job-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scrape-job-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-scrape-job-status?${params}`, {
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
      "error": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The data of the scrape. |
| `data.html` | string | HTML version of the content on page if `html` is in `formats` |
| `data.links` | array<string> | List of links on the page if `links` is in `formats` |
| `data.markdown` | string |  |
| `data.metadata` | object |  |
| `data.metadata.<any other metadata>` | string |  |
| `data.metadata.description` | string |  |
| `data.metadata.error` | string | The error message of the page |
| `data.metadata.language` | string |  |
| `data.metadata.sourceURL` | string |  |
| `data.metadata.statusCode` | number | The status code of the page |
| `data.metadata.title` | string |  |
| `data.rawHtml` | string | Raw HTML content of the page if `rawHtml` is in `formats` |
| `data.screenshot` | string | Screenshot of the page if `screenshot` is in `formats` |
| `error` | string | Error message |
| `status` | string | The current status of the crawl. Can be `scraping`, `completed`, or `failed`. |
| `success` | boolean |  |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v1/crawler/scrape/:id` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scrape-job-status.md) for the provider-specific parameters and requirements.

