# Bland AI: Analyze Call With AI

Retrieves AI analysis for a call in Bland AI.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/analyze-call-with-ai
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/analyze-call-with-ai?connectionId=$CONNECTION_ID&callId=string&goal=string&questions=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "callId": "string",
  "goal": "string",
  "questions": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/analyze-call-with-ai?${params}`, {
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
| `callId` | string | yes |  |
| `goal` | string | yes |  |
| `questions` | object<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answers": [
        "string"
      ],
      "credits_used": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answers` | array |  |
| `credits_used` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Bland AI API, this operation is `POST /v1/calls/{call_id}/analyze` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-call-with-ai.md) for the provider-specific parameters and requirements.

