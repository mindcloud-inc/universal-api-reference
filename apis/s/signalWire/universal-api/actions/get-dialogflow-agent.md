# SignalWire: Get Dialogflow Agent

Retrieves a Dialogflow agent from SignalWire.

```
GET https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-dialogflow-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SignalWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-dialogflow-agent?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signalWire/latest/actions/get-dialogflow-agent?${params}`, {
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
| `id` | string | yes | Unique ID of a Dialogflow Agent. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "dialogflow_agent": {
        "dialogflow_reference_id": "string",
        "dialogflow_reference_name": "Ava Chen",
        "display_name": "Ava Chen",
        "id": "string",
        "say": "string",
        "say_enabled": true,
        "voice": "string"
      },
      "display_name": "Ava Chen",
      "id": "string",
      "project_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Date and time when the resource was created. |
| `dialogflow_agent.dialogflow_reference_id` | string | Dialogflow reference ID |
| `dialogflow_agent.dialogflow_reference_name` | string | Dialogflow reference name |
| `dialogflow_agent.display_name` | string | Display name of the Dialogflow Agent |
| `dialogflow_agent.id` | string | Unique ID of a Dialogflow Agent. |
| `dialogflow_agent.say` | string | Default message to say |
| `dialogflow_agent.say_enabled` | boolean | Whether to enable the 'say' feature |
| `dialogflow_agent.voice` | string | Voice to use for speech |
| `display_name` | string | Display name of the Dialogflow Agent Fabric Resource |
| `id` | string | Unique ID of the Dialogflow Agent. |
| `project_id` | string | Unique ID of the Project. |
| `type` | string | Type of the Fabric Resource |
| `updated_at` | date | Date and time when the resource was updated. |

## Native endpoint

Through the native SignalWire API, this operation is `GET /fabric/resources/dialogflow_agents/{id}` (base URL `https://mindcloud.signalwire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dialogflow-agent.md) for the provider-specific parameters and requirements.

