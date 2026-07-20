# SVAHNAR: Delete Multiple Agents

Deletes multiple agents from SVAHNAR.

```
DELETE https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-multiple-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-multiple-agents?connectionId=$CONNECTION_ID&agentIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-multiple-agents?${params}`, {
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
| `agentIds[]` | array<string> | yes | The list of agent IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted_ids": [
        "string"
      ],
      "error_details": [
        {}
      ],
      "message": "string",
      "request_metadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted_ids` | array<string> | IDs of the agents that were successfully deleted. |
| `error_details` | array<object> | Per-agent failure details when deletion is only partially successful. |
| `message` | string | Summary of the bulk deletion operation. |
| `request_metadata` | object | Response metadata including the request ID. |

## Native endpoint

Through the native SVAHNAR API, this operation is `DELETE /v1/agents/bulk-delete` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-agents.md) for the provider-specific parameters and requirements.

