# DONNAJAMES Easy: Fetch All Agents

Retrieves all agents for a chatbot from DONNAJAMES Easy.

```
GET https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-agents?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/fetch-all-agents?${params}`, {
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
| `uuid` | string | yes | Chatbot uuid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "enabled": true,
      "meta": {},
      "modified_at": "string",
      "name": "Ava Chen",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `meta` | object |  |
| `modified_at` | string |  |
| `name` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native DONNAJAMES Easy API, this operation is `GET chatbot/:uuid/agents` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-all-agents.md) for the provider-specific parameters and requirements.

