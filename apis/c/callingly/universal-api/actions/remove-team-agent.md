# Callingly: Remove Team Agent

Deletes a team agent from Callingly.

```
DELETE https://connect.mindcloud.co/v1/universal/callingly/latest/actions/remove-team-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/remove-team-agent?connectionId=$CONNECTION_ID&id=string&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/remove-team-agent?${params}`, {
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
| `id` | string | yes |  |
| `agentId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Callingly API returns.

## Native endpoint

Through the native Callingly API, this operation is `DELETE /v1/teams/{{id}}/agents/{{agent_id}}` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-agent.md) for the provider-specific parameters and requirements.

