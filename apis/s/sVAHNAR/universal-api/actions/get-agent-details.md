# SVAHNAR: Get Agent Details

Retrieves agent details from SVAHNAR.

```
GET https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SVAHNAR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-details?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sVAHNAR/latest/actions/get-agent-details?${params}`, {
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
| `agentId` | string | yes | The unique identifier of the agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent_id": "string",
      "description": "string",
      "hosted_to": "string",
      "is_creator": true,
      "name": "Ava Chen",
      "request_metadata": {},
      "uploaded_by": {},
      "yaml_configuration": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent_id` | string | Unique identifier of the agent. |
| `description` | string | Description of the agent. |
| `hosted_to` | string | Deployment target for the agent. |
| `is_creator` | boolean | Whether the authenticated user is the creator of the agent. |
| `name` | string | Name of the agent. |
| `request_metadata` | object | Response metadata including the request ID. |
| `uploaded_by` | object | Information about the agent creator. |
| `yaml_configuration` | string | Provider note describing how to retrieve the YAML configuration. |

## Native endpoint

Through the native SVAHNAR API, this operation is `GET /v1/agents/get-agent/:agent_id` (base URL `https://api.svahnar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-details.md) for the provider-specific parameters and requirements.

