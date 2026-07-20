# Olostep: Get Scrape

Retrieves details for a scrape in Olostep.

```
GET https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-scrape
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-scrape?connectionId=$CONNECTION_ID&scrapeId=scrape_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scrapeId": "scrape_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-scrape?${params}`, {
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
| `scrapeId` | string | yes | The ID of the scrape to retrieve. Example: `scrape_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "object": "string",
      "result": {
        "htmlContent": "string",
        "htmlHostedUrl": "https://example.com",
        "jsonContent": {},
        "jsonHostedUrl": {},
        "linksOnPage": [
          "https://example.com"
        ],
        "markdownContent": "string",
        "markdownHostedUrl": "https://example.com",
        "pageMetadata": {
          "statusCode": 1,
          "title": "string"
        },
        "screenshotHostedUrl": {},
        "textHostedUrl": {}
      },
      "retrieveId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `id` | string |  |
| `object` | string |  |
| `result.htmlContent` | string |  |
| `result.htmlHostedUrl` | string |  |
| `result.jsonContent` | object |  |
| `result.jsonHostedUrl` | object |  |
| `result.linksOnPage[]` | string |  |
| `result.markdownContent` | string |  |
| `result.markdownHostedUrl` | string |  |
| `result.pageMetadata.statusCode` | number |  |
| `result.pageMetadata.title` | string |  |
| `result.screenshotHostedUrl` | object |  |
| `result.textHostedUrl` | object |  |
| `retrieveId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `GET /v1/scrapes/[:scrape_id]` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scrape.md) for the provider-specific parameters and requirements.

