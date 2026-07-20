# Chatvolt AI: Get Mercado Livre Products

Retrieves Mercado Livre products from Chatvolt AI.

```
GET https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/mercadolivre-get-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/mercadolivre-get-products?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/mercadolivre-get-products?${params}`, {
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
| `agentId` | string | yes | The ID of the agent. |
| `query` | string | no | The search query for fuzzy search. |
| `threshold` | number | no | The threshold for fuzzy search. |
| `maxResults` | number | no | The maximum number of results to return. |
| `caseSensitive` | boolean | no | Whether the search should be case-sensitive. |
| `sortByRelevance` | boolean | no | Whether to sort the results by relevance. |
| `partialMatch` | boolean | no | Whether to allow partial matches. |
| `typoTolerance` | number | no | The typo tolerance for fuzzy search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<string> | Response items. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `GET /mercadolivre/get-products` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mercadolivre-get-products.md) for the provider-specific parameters and requirements.

