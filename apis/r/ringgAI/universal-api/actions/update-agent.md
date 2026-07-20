# Ringg AI: Update Agent

Updates an existing agent in Ringg AI.

```
PUT https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | (Required) The unique ID of the agent to update |
| `agentName` | string | no | (Optional) Name of the agent |
| `introductionAndObjective` | string | no | (Optional) Introduction and objective of the agent |
| `responseGuidelines` | string | no | (Optional) Guidelines for how the agent should respond |
| `task` | string | no | (Optional) The task the agent should perform |
| `faq` | string | no | (Optional) FAQ content for the agent |
| `sampleConversations` | string | no | (Optional) Example conversations for the agent. Use \n for newlines between turns. |
| `primaryLanguage` | string | no | (Optional) Primary language locale for the agent |
| `secondaryLanguage` | string | no | (Optional) Secondary language locale for the agent |
| `voiceId` | string | no | (Optional) Internal AgentVoice ID (UUID). Get available voices from the Get Assistant Voices endpoint. |
| `introMessage` | string | no | (Optional) Introduction message the agent will speak when the call starts |
| `agentType` | string | no | (Optional) Type of agent |
| `customVariables[]` | array<string> | no | (Optional) Custom variables for the agent. For outbound agents, callee_name and mobile_number cannot be removed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "version": "string"
      },
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.id` | string | The unique ID of the updated agent |
| `data.updatedAt` | date |  |
| `data.version` | string | The version slug of the agent |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Ringg AI API, this operation is `PATCH /public/agent/:agent_id` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

