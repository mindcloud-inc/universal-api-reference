# Brand.dev: Scrape URL and Convert to Markdown

Retrieves markdown from a URL using Brand.dev.

```
GET https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-url-and-convert-to-markdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brand.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-url-and-convert-to-markdown?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-url-and-convert-to-markdown?${params}`, {
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
| `url` | string | yes | Full URL to scrape and convert to Markdown. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "markdown": "string",
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `markdown` | string |  |
| `success` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Brand.dev API, this operation is `GET /web/scrape/markdown` (base URL `https://api.brand.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-url-and-convert-to-markdown.md) for the provider-specific parameters and requirements.

