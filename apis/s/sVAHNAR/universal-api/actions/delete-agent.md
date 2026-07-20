# SVAHNAR: Delete Agent

Deletes an existing agent from SVAHNAR.

```
DELETE https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-agent?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/delete-agent?${params}`, {
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
| `agentId` | string | yes | The unique identifier of the agent to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted_id": "string",
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
| `deleted_id` | string | ID of the agent that was successfully deleted. |
| `message` | string | Summary of the deletion operation. |
| `request_metadata` | object | Response metadata including the request ID. |

## Native endpoint

Through the native SVAHNAR API, this operation is `DELETE /v1/agents/delete` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-agent.md) for the provider-specific parameters and requirements.

