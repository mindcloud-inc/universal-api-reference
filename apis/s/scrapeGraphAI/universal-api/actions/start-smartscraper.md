# ScrapeGraphAI: Start SmartScraper

Starts a SmartScraper extraction job in ScrapeGraphAI.

```
POST https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartscraper
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeGraphAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartscraper" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userPrompt": "Extract the company name and one-sentence description",
  "websiteUrl": "https://scrapegraphai.com/"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapeGraphAI/latest/actions/start-smartscraper', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userPrompt": "Extract the company name and one-sentence description",
    "websiteUrl": "https://scrapegraphai.com/"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userPrompt` | string | yes | Natural language description of what to extract from the page. Example: `Extract the company name and one-sentence description`. |
| `websiteUrl` | string | yes | URL of the webpage to extract information from. Example: `https://scrapegraphai.com/`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cookies` | object | no | Optional cookies object for authenticated pages or session state. Example: `[object Object]`. |
| `headers` | object | no | Optional custom HTTP headers to send with the request. Example: `[object Object]`. |
| `mock` | boolean | no | Return mock data instead of performing a live extraction. Default: `false`. |
| `numberOfScrolls` | number | no | Number of times to scroll for infinite-scroll pages before extraction. Example: `3`. |
| `outputSchema` | object | no | Optional schema object to structure the extracted output. Example: `[object Object]`. |
| `plainText` | boolean | no | Return plain text instead of structured JSON output. Default: `false`. |
| `stealth` | boolean | no | Enable stealth mode to bypass bot protection. Default: `false`. |
| `steps[]` | array<string> | no | Optional interaction steps to perform on the page before extraction. Example: `click on filter button,wait for results`. |
| `totalPages` | number | no | Number of pages to extract when pagination is needed. Example: `2`. |
| `websiteHtml` | string | no | Raw HTML content to process directly, mutually exclusive with Website URL and Website Markdown. Example: `<html><body><h1>Title</h1></body></html>`. |
| `websiteMarkdown` | string | no | Raw Markdown content to process directly, mutually exclusive with Website URL and Website HTML. Example: `# Title\n\nSome markdown content`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "requestId": "string",
      "result": {},
      "status": "string",
      "userPrompt": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message, empty when successful. |
| `requestId` | string | Unique identifier for the SmartScraper request. |
| `result` | object | Extraction result payload. |
| `status` | string | Current status of the request. |
| `userPrompt` | string | Original extraction prompt. |
| `websiteUrl` | string | Website URL processed by the request. |

## Native endpoint

Through the native ScrapeGraphAI API, this operation is `POST /smartscraper` (base URL `https://api.scrapegraphai.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-smartscraper.md) for the provider-specific parameters and requirements.

