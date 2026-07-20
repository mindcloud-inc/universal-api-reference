# ScrapingDog: Get Google AI Overview

Retrieves Google AI Overview results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-overview
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-overview?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-ai-overview?${params}`, {
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
| `query` | string | yes | Search query to run for Google AI Overview. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_overview": {
        "references": {
          "index": 1,
          "link": "https://example.com",
          "logo": "string",
          "snippet": "string",
          "source": "string",
          "title": "string"
        },
        "text_blocks": {
          "snippet": "string",
          "snippet_highlighted_words": "string",
          "type": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_overview` | object |  |
| `ai_overview.references` | array<object> |  |
| `ai_overview.references.index` | number |  |
| `ai_overview.references.link` | string |  |
| `ai_overview.references.logo` | string |  |
| `ai_overview.references.snippet` | string |  |
| `ai_overview.references.source` | string |  |
| `ai_overview.references.title` | string |  |
| `ai_overview.text_blocks` | array<object> |  |
| `ai_overview.text_blocks.snippet` | string |  |
| `ai_overview.text_blocks.snippet_highlighted_words` | string |  |
| `ai_overview.text_blocks.type` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google/ai_overview` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-ai-overview.md) for the provider-specific parameters and requirements.

