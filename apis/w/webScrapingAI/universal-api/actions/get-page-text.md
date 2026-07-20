# WebScraping.AI: Get Page Text



```
GET https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebScraping.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-text?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-text?${params}`, {
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
| `url` | string | yes | Target webpage URL |
| `textFormat` | string | no | Format of the text response: plain, json, or xml |
| `returnLinks` | boolean | no | Include links in the JSON response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "description": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `description` | string |  |
| `title` | string |  |

## Native endpoint

Through the native WebScraping.AI API, this operation is `GET /text` (base URL `https://api.webscraping.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-text.md) for the provider-specific parameters and requirements.

