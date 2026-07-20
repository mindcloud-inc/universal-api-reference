# WebScraping.AI: Get Selected HTML For Multiple Selectors



```
GET https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html-for-multiple-selectors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraping.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html-for-multiple-selectors?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&selectors=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "selectors": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-selected-html-for-multiple-selectors?${params}`, {
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
| `url` | string | yes | URL of the webpage to fetch selected HTML fragments from. |
| `selectors` | string<string> | yes | CSS selectors for the HTML fragments to return. Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebScraping.AI API returns.

## Native endpoint

Through the native WebScraping.AI API, this operation is `GET /selected-multiple` (base URL `https://api.webscraping.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-selected-html-for-multiple-selectors.md) for the provider-specific parameters and requirements.

