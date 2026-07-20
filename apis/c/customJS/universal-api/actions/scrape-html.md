# CustomJS: Scrape HTML

Retrieves HTML content from a website using CustomJS.

```
GET https://connect.mindcloud.co/v1/universal/customJS/latest/actions/scrape-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomJS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/scrape-html?connectionId=$CONNECTION_ID&input.url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input.url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customJS/latest/actions/scrape-html?${params}`, {
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
| `input.url` | string | yes | Website URL to scrape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string |  |

## Native endpoint

Through the native CustomJS API, this operation is `POST https://e.customjs.io/scraper` (base URL `https://e.customjs.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scrape-html.md) for the provider-specific parameters and requirements.

