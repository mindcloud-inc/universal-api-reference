# PreCallAI: List Assistants

Retrieves assistants from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-assistants?${params}`, {
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
      "data": {
        "ai_model_id": 1,
        "company_name": "Ava Chen",
        "goal": "string",
        "id": "string",
        "language": "string",
        "name": "Ava Chen",
        "type": "string",
        "voice_id": "string",
        "voice_name": "Ava Chen"
      },
      "message": "string",
      "status": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of assistants returned by PreCallAI. |
| `data.ai_model_id` | number | AI model ID used by the assistant. |
| `data.company_name` | string | Company name associated with the assistant. |
| `data.goal` | string | Assistant goal. |
| `data.id` | string | Assistant ID. |
| `data.language` | string | Assistant language. |
| `data.name` | string | Assistant name. |
| `data.type` | string | Assistant type. |
| `data.voice_id` | string | Voice resource ID used by the assistant. |
| `data.voice_name` | string | Voice name used by the assistant. |
| `message` | string | Provider status message for listing assistants. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the assistant list request succeeded. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /user/listAssistant` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assistants.md) for the provider-specific parameters and requirements.

