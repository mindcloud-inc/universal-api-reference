# Claid AI: Get AI Edit Generation Result

Retrieves an AI image edit result from Claid AI.

```
GET https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-ai-edit-generation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-ai-edit-generation-result?connectionId=$CONNECTION_ID&aiEditId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "aiEditId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/get-ai-edit-generation-result?${params}`, {
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
| `aiEditId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "errors": [
        {}
      ],
      "id": 1,
      "request": {},
      "result": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Request creation timestamp. |
| `errors` | array<object> | Processing errors, if any. |
| `id` | number | Task identifier. |
| `request` | object | Echoed request payload. |
| `result` | object | Input and output image details. |
| `status` | string | Current processing status. |

## Native endpoint

Through the native Claid AI API, this operation is `GET image/ai-edit/:ai_edit_id` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ai-edit-generation-result.md) for the provider-specific parameters and requirements.

