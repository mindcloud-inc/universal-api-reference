# Olostep: Create Scrape

Creates a new scrape in Olostep.

```
POST https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-scrape
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Olostep `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-scrape" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlToScrape": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/olostep/latest/actions/create-scrape', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlToScrape": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlToScrape` | string | yes | The URL to start scraping from. Example: `https://example.com`. |
| `formats[]` | array<string> | no | Optional formats in which to return content. One of: `0`, `1`, `2`, `3`, `4`, `5`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creditsConsumed": 1,
      "id": "string",
      "object": "string",
      "result": {
        "fileHostedUrl": {},
        "htmlContent": {},
        "htmlHostedUrl": {},
        "imageQueued": {},
        "jsonContent": {},
        "jsonHostedUrl": {},
        "markdownContent": "string",
        "markdownHostedUrl": "https://example.com",
        "networkCalls": {},
        "pageMetadata": {
          "statusCode": 1
        },
        "screenshotHostedUrl": {},
        "sizeExceeded": true,
        "textContent": {},
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
| `creditsConsumed` | number |  |
| `id` | string |  |
| `object` | string |  |
| `result.fileHostedUrl` | object |  |
| `result.htmlContent` | object |  |
| `result.htmlHostedUrl` | object |  |
| `result.imageQueued` | object |  |
| `result.jsonContent` | object |  |
| `result.jsonHostedUrl` | object |  |
| `result.markdownContent` | string |  |
| `result.markdownHostedUrl` | string |  |
| `result.networkCalls` | object |  |
| `result.pageMetadata.statusCode` | number |  |
| `result.screenshotHostedUrl` | object |  |
| `result.sizeExceeded` | boolean |  |
| `result.textContent` | object |  |
| `result.textHostedUrl` | object |  |
| `retrieveId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Olostep API, this operation is `POST /v1/scrapes` (base URL `https://api.olostep.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scrape.md) for the provider-specific parameters and requirements.

