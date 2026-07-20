# WebScraping.AI: Extract Structured Fields



```
GET https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/extract-structured-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraping.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/extract-structured-fields?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&fields=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "fields": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/extract-structured-fields?${params}`, {
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
| `url` | string | yes | URL of the webpage to extract structured fields from. |
| `fields` | object | yes | Field-to-description object used to tell WebScraping.AI what structured values to extract. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebScraping.AI API returns.

## Native endpoint

Through the native WebScraping.AI API, this operation is `GET /ai/fields` (base URL `https://api.webscraping.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-structured-fields.md) for the provider-specific parameters and requirements.

