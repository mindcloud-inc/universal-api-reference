# ScrapeGraphAI: Start Markdownify

Starts a Markdownify conversion job in ScrapeGraphAI.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-markdownify
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-markdownify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteUrl": "https://scrapegraphai.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-markdownify', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteUrl": "https://scrapegraphai.com/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `websiteUrl` | string | yes | URL of the webpage to convert to Markdown. Example: `https://scrapegraphai.com/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | object | no | Optional custom HTTP headers to send with the request. Example: `[object Object]`. |
| `stealth` | boolean | no | Enable stealth mode to bypass bot protection. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "requestId": "string",
      "result": "string",
      "status": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message when the request fails. |
| `requestId` | string | Unique identifier for the Markdownify request. |
| `result` | string | Markdownified webpage content. |
| `status` | string | Current status of the request. |
| `websiteUrl` | string | Website URL converted to Markdown. |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /markdownify` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-markdownify.md) for the provider-specific parameters and requirements.

