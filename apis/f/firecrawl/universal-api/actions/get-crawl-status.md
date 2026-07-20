# Firecrawl: Get Crawl Status

Retrieves crawl job status from Firecrawl.

```
GET https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-crawl-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firecrawl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-crawl-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/get-crawl-status?${params}`, {
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
| `id` | string | yes | The ID of the crawl job |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completed": 1,
      "creditsUsed": 1,
      "data": {
        "markdown": "string",
        "metadata": {
          "cachedAt": "2026-05-07T12:00:00.000Z",
          "cacheState": "string",
          "contentType": "string",
          "creditsUsed": 1,
          "language": "string",
          "proxyUsed": "string",
          "scrapeId": "string",
          "sourceURL": "https://example.com",
          "statusCode": 1,
          "title": "string",
          "url": "https://example.com",
          "viewport": "string"
        }
      },
      "expiresAt": "2026-05-07T12:00:00.000Z",
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
| `completed` | number |  |
| `creditsUsed` | number |  |
| `data` | array<object> |  |
| `data.markdown` | string |  |
| `data.metadata.cachedAt` | date |  |
| `data.metadata.cacheState` | string |  |
| `data.metadata.contentType` | string |  |
| `data.metadata.creditsUsed` | number |  |
| `data.metadata.language` | string |  |
| `data.metadata.proxyUsed` | string |  |
| `data.metadata.scrapeId` | string |  |
| `data.metadata.sourceURL` | string |  |
| `data.metadata.statusCode` | number |  |
| `data.metadata.title` | string |  |
| `data.metadata.url` | string |  |
| `data.metadata.viewport` | string |  |
| `expiresAt` | date |  |
| `status` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Firecrawl API, this operation is `GET /crawl/:id` (base URL `https://api.firecrawl.dev/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-crawl-status.md) for the provider-specific parameters and requirements.

