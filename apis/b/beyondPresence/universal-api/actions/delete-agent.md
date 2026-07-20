# Beyond Presence: Delete Agent

Deletes an existing agent from Beyond Presence.

```
DELETE https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/delete-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/delete-agent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/delete-agent?${params}`, {
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
| `id` | string | yes | Agent ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beyond Presence API returns.

## Native endpoint

Through the native Beyond Presence API, this operation is `DELETE /v1/agents/:id` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent.md) for the provider-specific parameters and requirements.

