# MessageBird: Delete Allow/Block Rule



```
DELETE https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/delete-allowblock-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/delete-allowblock-rule?connectionId=$CONNECTION_ID&workspaceId=string&allowBlockRuleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "allowBlockRuleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/delete-allowblock-rule?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the allow/block rule. |
| `allowBlockRuleId` | string | yes | The Bird allow/block rule ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MessageBird API returns.

## Native endpoint

Through the native MessageBird API, this operation is `DELETE /workspaces/:workspaceId/conversation-allowblock-rules/:allowBlockRuleId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-allowblock-rule.md) for the provider-specific parameters and requirements.

