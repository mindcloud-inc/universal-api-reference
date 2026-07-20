# DONNAJAMES Easy: Create Agent

Creates a new agent for a chatbot in DONNAJAMES Easy.

```
POST https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DONNAJAMES Easy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dONNAJAMESEasy/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string",
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no |  |
| `model` | string | no |  |
| `prompt` | string | no |  |
| `uuid` | string | yes | Chatbot uuid |
| `name` | string | yes |  |
| `type` | string | yes |  |
| `temperature` | number | no |  |
| `useAllSources` | boolean | no |  |

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

Through the native DONNAJAMES Easy API, this operation is `POST chatbot/:uuid/agent/create` (base URL `https://app.gpt-trainer.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

