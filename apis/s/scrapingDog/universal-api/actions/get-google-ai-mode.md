# ScrapingDog: Get Google AI Mode

Retrieves Google AI Mode results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-mode?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-mode?${params}`, {
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
| `query` | string | yes | Search query to run for Google AI Mode. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "references": {
        "index": 1,
        "link": "https://example.com",
        "snippet": "string",
        "source": "string",
        "title": "string"
      },
      "textBlocks": {
        "snippet": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `references` | array<object> |  |
| `references.index` | number |  |
| `references.link` | string |  |
| `references.snippet` | string |  |
| `references.source` | string |  |
| `references.title` | string |  |
| `textBlocks` | array<object> |  |
| `textBlocks.snippet` | string |  |
| `textBlocks.type` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google/ai_mode` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-ai-mode.md) for the provider-specific parameters and requirements.

