# Open AI: Compact Response

Compacts a response in Open AI.

```
POST https://connect.mindcloud.co/v1/universal/openAi/latest/actions/compact-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openAi/latest/actions/compact-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input[]": [
    {
      "role": "user",
      "content": [
        {
          "text": "Summarize the OpenAI API in one sentence.",
          "type": "input_text"
        }
      ]
    }
  ],
  "model": "gpt-4.1-mini"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openAi/latest/actions/compact-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input[]": [{"role":"user","content":[{"text":"Summarize the OpenAI API in one sentence.","type":"input_text"}]}],
    "model": "gpt-4.1-mini"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `input[]` | array<object> | yes | Conversation input to compact. Default: `[{"role":"user","content":[{"text":"Summarize the OpenAI API in one sentence.","type":"input_text"}]}]`. |
| `model` | string | yes | Model ID used for compaction. Default: `gpt-4.1-mini`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {
          "id": "string",
          "type": "string"
        }
      ],
      "usage": {
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | number | Unix creation timestamp. |
| `id` | string | Compacted response ID. |
| `model` | string | Model used for compaction. |
| `object` | string | Response object type. |
| `output[].id` | string | Output item ID. |
| `output[].type` | string | Output item type. |
| `usage.total_tokens` | number | Total tokens after compaction. |

## Native endpoint

Through the native Open AI API, this operation is `POST v1/responses/compact` (base URL `https://api.openai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compact-response.md) for the provider-specific parameters and requirements.

