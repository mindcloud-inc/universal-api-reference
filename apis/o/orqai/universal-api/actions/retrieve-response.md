# Orq.ai: Retrieve Response

Retrieves a response from Orq.ai.

```
GET https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-response?connectionId=$CONNECTION_ID&responseId=orq_resp_test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "responseId": "orq_resp_test"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/retrieve-response?${params}`, {
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
| `responseId` | string | yes | Response ID from the Orq.ai path parameter. Example: `orq_resp_test`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "background": true,
      "completedAt": 1,
      "createdAt": 1,
      "id": "string",
      "input": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "id": "string",
          "role": "string",
          "type": "string"
        }
      ],
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
      "temperature": 1,
      "tools": [
        {
          "type": "string"
        }
      ],
      "topP": 1,
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
| `background` | boolean |  |
| `completedAt` | number |  |
| `createdAt` | number |  |
| `id` | string |  |
| `input[].content[].text` | string |  |
| `input[].content[].type` | string |  |
| `input[].id` | string |  |
| `input[].role` | string |  |
| `input[].type` | string |  |
| `model` | string |  |
| `object` | string |  |
| `output[].content[].text` | string |  |
| `output[].content[].type` | string |  |
| `output[].id` | string |  |
| `output[].role` | string |  |
| `output[].status` | string |  |
| `output[].type` | string |  |
| `status` | string |  |
| `temperature` | number |  |
| `tools[].type` | string |  |
| `topP` | number |  |
| `usage.inputTokens` | number |  |
| `usage.outputTokens` | number |  |
| `usage.totalTokens` | number |  |

## Native endpoint

Through the native Orq.ai API, this operation is `GET /v3/router/responses/[:response_id]` (base URL `https://api.orq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-response.md) for the provider-specific parameters and requirements.

