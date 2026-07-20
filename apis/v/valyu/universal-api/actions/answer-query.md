# Valyu: Answer Query



```
GET https://connect.mindcloud.co/v1/universal/valyu/latest/actions/answer-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/answer-query?connectionId=$CONNECTION_ID&query=Ask%20a%20question%20to%20answer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Ask a question to answer"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/valyu/latest/actions/answer-query?${params}`, {
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
| `query` | string | yes | The question or research query to answer. Example: `Ask a question to answer`. |
| `search_type` | string | no | Controls which data sources are searched for the answer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_usage": {},
      "contents": "string",
      "cost": {},
      "original_query": "string",
      "search_metadata": {},
      "search_results": [
        {}
      ],
      "success": true,
      "tx_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_usage` | object |  |
| `contents` | string |  |
| `cost` | object |  |
| `original_query` | string |  |
| `search_metadata` | object |  |
| `search_results` | array<object> |  |
| `success` | boolean |  |
| `tx_id` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /answer` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/answer-query.md) for the provider-specific parameters and requirements.

