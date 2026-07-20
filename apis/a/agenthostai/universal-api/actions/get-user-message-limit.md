# Agenthost.ai: Get User Message Limit

Retrieves a user's message limit from Agenthost.ai.

```
GET https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agenthost.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/get-user-message-limit?${params}`, {
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
| `email` | string | no | Optional email address to check a specific user's message limit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | string | The number of messages the user can send. |

## Native endpoint

Through the native Agenthost.ai API, this operation is `POST /api/openai/user_message_limit/` (base URL `https://api.agenthost.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-message-limit.md) for the provider-specific parameters and requirements.

