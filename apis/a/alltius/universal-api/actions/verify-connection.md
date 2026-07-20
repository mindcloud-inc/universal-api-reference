# Alltius: Verify Connection

Submits a test prompt to verify an Alltius connection.

```
GET https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alltius `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alltius/latest/actions/verify-connection?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_confidence_score": 1,
      "answer_type": "string",
      "blocks_response": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_at_response": "2026-05-07T12:00:00.000Z",
      "cta_list": {},
      "id": "string",
      "image_metadata_list": [
        {}
      ],
      "intent_confidence": 1,
      "intent_confidence_label": "string",
      "intent_type": "string",
      "llm_response_model_family": "string",
      "metadata": {},
      "multi_cta_list": [
        {}
      ],
      "post": "string",
      "rating": 1,
      "recommendations": [
        {}
      ],
      "relevant_links_response": "https://example.com",
      "response": "string",
      "thread_id": "string",
      "v2_chat_session_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer_confidence_score` | number |  |
| `answer_type` | string |  |
| `blocks_response` | object |  |
| `created_at` | date |  |
| `created_at_response` | date |  |
| `cta_list` | object |  |
| `id` | string |  |
| `image_metadata_list` | array<object> |  |
| `intent_confidence` | number |  |
| `intent_confidence_label` | string |  |
| `intent_type` | string |  |
| `llm_response_model_family` | string |  |
| `metadata` | object |  |
| `multi_cta_list` | array<object> |  |
| `post` | string |  |
| `rating` | number |  |
| `recommendations` | array<object> |  |
| `relevant_links_response` | string |  |
| `response` | string |  |
| `thread_id` | string |  |
| `v2_chat_session_id` | string |  |

## Native endpoint

Through the native Alltius API, this operation is `POST /v1/chat` (base URL `https://app.alltius.ai/api/platform`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-connection.md) for the provider-specific parameters and requirements.

