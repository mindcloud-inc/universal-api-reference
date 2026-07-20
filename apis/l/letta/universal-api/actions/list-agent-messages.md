# Letta: List Agent Messages

Retrieves messages from an agent in Letta.

```
GET https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-agent-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-agent-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-agent-messages?${params}`, {
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
| `agentId` | string | yes | The Letta agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "message_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `date` | date |  |
| `id` | string |  |
| `message_type` | string |  |

## Native endpoint

Through the native Letta API, this operation is `GET /v1/agents/:agent_id/messages` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-agent-messages.md) for the provider-specific parameters and requirements.

