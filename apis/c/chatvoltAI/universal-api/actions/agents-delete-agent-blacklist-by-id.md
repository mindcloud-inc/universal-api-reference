# Chatvolt AI: Delete Agent Blacklist Entry

Deletes an agent blacklist entry from Chatvolt AI.

```
DELETE https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-agent-blacklist-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-agent-blacklist-by-id?connectionId=$CONNECTION_ID&agentId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/agents-delete-agent-blacklist-by-id?${params}`, {
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
| `agentId` | string | yes | The ID of the agent associated with the blacklist (required for path, but not used in delete logic). |
| `id` | string | yes | The ID of the blacklist entry to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatvolt AI API returns.

## Native endpoint

Through the native Chatvolt AI API, this operation is `DELETE /agent-blacklist/{agentId}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/agents-delete-agent-blacklist-by-id.md) for the provider-specific parameters and requirements.

