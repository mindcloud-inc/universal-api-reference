# eGain: Update Orchestration

Updates an existing orchestration in eGain.

```
PUT https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-orchestration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eGain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-orchestration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "active": true,
  "applications.botConfiguration.bots[0].id": "string",
  "applications.botConfiguration.bots[0].onEscalation.agent.id": "string",
  "applications.botConfiguration.bots[0].participant.id": "string",
  "applications.customerConfiguration.customer.id": "string",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eGain/latest/actions/update-orchestration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "active": true,
    "applications.botConfiguration.bots[0].id": "string",
    "applications.botConfiguration.bots[0].onEscalation.agent.id": "string",
    "applications.botConfiguration.bots[0].participant.id": "string",
    "applications.customerConfiguration.customer.id": "string",
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `active` | boolean | yes | Whether orchestration is active. |
| `applications.botConfiguration.bots[0].id` | string | yes | Bot app ID. |
| `applications.botConfiguration.bots[0].onEscalation.agent.id` | string | yes | Escalation agent app ID. |
| `applications.botConfiguration.bots[0].participant.id` | string | yes | Bot participant ID. |
| `applications.customerConfiguration.customer.id` | string | yes | Customer app ID. |
| `description` | string | no | Orchestration description. |
| `id` | string | yes | Orchestration ID. |
| `name` | string | yes | Orchestration name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eGain API returns.

## Native endpoint

Through the native eGain API, this operation is `PUT /orchestrations/:id` (base URL `https://api.ai.egain.cloud/conversation/conversationmgr/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-orchestration.md) for the provider-specific parameters and requirements.

