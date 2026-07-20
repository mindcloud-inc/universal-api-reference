# Cursor: Get Agent Conversation



```
GET https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-conversation?connectionId=$CONNECTION_ID&id=bc_abc123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "bc_abc123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cursor/latest/actions/get-agent-conversation?${params}`, {
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
| `id` | string | yes | Unique identifier for the cloud agent conversation to retrieve. Example: `bc_abc123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Message identifier. |
| `text` | string | Message content. |
| `type` | string | Message type: user_message or assistant_message. |

## Native endpoint

Through the native Cursor API, this operation is `GET /v0/agents/{{id}}/conversation` (base URL `https://api.cursor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-conversation.md) for the provider-specific parameters and requirements.

