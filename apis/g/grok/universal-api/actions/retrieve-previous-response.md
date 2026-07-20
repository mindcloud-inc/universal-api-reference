# Grok: Retrieve Previous Response

Retrieves a previous response from Grok.

```
GET https://connect.mindcloud.co/v1/universal/grok/latest/actions/retrieve-previous-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grok/latest/actions/retrieve-previous-response?connectionId=$CONNECTION_ID&responseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "responseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grok/latest/actions/retrieve-previous-response?${params}`, {
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
| `responseId` | string | yes | Response identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": 1,
      "createdAt": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "status": "string",
          "type": "string"
        }
      ],
      "status": "string",
      "usage": {
        "inputTokens": 1,
        "outputTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | number | Unix timestamp when the response completed. |
| `createdAt` | number | Unix timestamp when the response was created. |
| `id` | string | Response identifier. |
| `model` | string | Model used to generate the response. |
| `object` | string | Provider object type. |
| `output` | array<object> | Generated output items returned by xAI. |
| `output[].content` | array<object> | Content blocks for the output item. |
| `output[].content[].text` | string | Rendered text for the content block. |
| `output[].content[].type` | string | Content block type. |
| `output[].id` | string | Message item identifier. |
| `output[].role` | string | Role for the output item. |
| `output[].status` | string | Completion status for the output item. |
| `output[].type` | string | Output item type. |
| `status` | string | Lifecycle status of the response. |
| `usage` | object | Token usage metadata for the response. |
| `usage.inputTokens` | number | Input token count. |
| `usage.outputTokens` | number | Output token count. |
| `usage.totalTokens` | number | Total token count. |

## Native endpoint

Through the native Grok API, this operation is `GET /v1/responses/:response_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-previous-response.md) for the provider-specific parameters and requirements.

