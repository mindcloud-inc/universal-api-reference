# LLMLayer: Scrape Website HTML

Retrieves scraped website content as HTML from LLMLayer.

```
GET https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/scrape-website-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LLMLayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/scrape-website-html?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/scrape-website-html?${params}`, {
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
| `url` | string | yes | Website URL to scrape. Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": 1,
      "html": "string",
      "markdown": "string",
      "metadata": {},
      "pdf": "string",
      "screenshot": "string",
      "statusCode": 1,
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | number | LLMLayer request cost. |
| `html` | string | HTML content extracted from the target page. |
| `markdown` | string | Markdown content extracted from the target page. |
| `metadata` | object | Additional metadata returned by LLMLayer. |
| `pdf` | string | PDF output when requested. |
| `screenshot` | string | Base64 screenshot output when requested. |
| `statusCode` | number | HTTP status code returned by the target page. |
| `title` | string | Resolved page title. |
| `url` | string | Scraped URL. |

## Native endpoint

Through the native LLMLayer API, this operation is `POST /api/v2/scrape` (base URL `https://api.llmlayer.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-website-html.md) for the provider-specific parameters and requirements.

