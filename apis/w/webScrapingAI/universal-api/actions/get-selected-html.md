# WebScraping.AI: Get Selected HTML



```
GET https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraping.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&selector=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "selector": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html?${params}`, {
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
| `url` | string | yes | URL of the webpage to fetch a selected HTML fragment from. |
| `selector` | string | yes | CSS selector for the HTML fragment to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native WebScraping.AI API, this operation is `GET /selected` (base URL `https://api.webscraping.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-selected-html.md) for the provider-specific parameters and requirements.

