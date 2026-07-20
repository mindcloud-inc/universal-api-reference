# Chatsistant: List Messages

Retrieves session message records from Chatsistant.

```
GET https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatsistant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatsistant/latest/actions/list-messages?${params}`, {
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
| `uuid` | string | no | The session UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ai_context_json": "string",
      "background_pending_tasks": 1,
      "cite_data_json": "string",
      "created_at": "string",
      "detected_frustrations": "string",
      "error_message": "string",
      "feedback_json": "string",
      "finish_reason": "string",
      "labels": [
        {}
      ],
      "meta_json": "string",
      "modified_at": "string",
      "query": "string",
      "response": "string",
      "session_documents": [
        {}
      ],
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ai_context_json` | string |  |
| `background_pending_tasks` | number |  |
| `cite_data_json` | string |  |
| `created_at` | string |  |
| `detected_frustrations` | string |  |
| `error_message` | string |  |
| `feedback_json` | string |  |
| `finish_reason` | string |  |
| `labels` | array<object> |  |
| `meta_json` | string |  |
| `modified_at` | string |  |
| `query` | string |  |
| `response` | string |  |
| `session_documents` | array<object> |  |
| `uuid` | string |  |

## Native endpoint

Through the native Chatsistant API, this operation is `GET /session/:uuid/messages` (base URL `https://app.chatsistant.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

