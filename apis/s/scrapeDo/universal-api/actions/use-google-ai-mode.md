# Scrape do: Use Google AI mode

Retrieves Google AI Mode results with Scrape do.

```
GET https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/use-google-ai-mode
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrape do `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/use-google-ai-mode?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeDo/latest/actions/use-google-ai-mode?${params}`, {
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
| `q` | string | yes | The Google AI mode query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "references": [
        {}
      ],
      "search_parameters": {},
      "shopping_results": [
        {}
      ],
      "text_blocks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `references` | array<object> | Referenced source entries. |
| `search_parameters` | object | Echo of AI mode request parameters. |
| `shopping_results` | array<object> | Shopping result entries when relevant. |
| `text_blocks` | array<object> | AI-generated content blocks. |

## Native endpoint

Through the native Scrape do API, this operation is `GET /plugin/google/search/ai-mode` (base URL `https://api.scrape.do`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/use-google-ai-mode.md) for the provider-specific parameters and requirements.

