# Ringg AI: Create Agent

Creates an agent in Ringg AI.

```
POST https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentName": "Ava Chen",
  "introductionAndObjective": "string",
  "responseGuidelines": "string",
  "task": "string",
  "primaryLanguage": "string",
  "voiceId": "string",
  "introMessage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentName": "Ava Chen",
    "introductionAndObjective": "string",
    "responseGuidelines": "string",
    "task": "string",
    "primaryLanguage": "string",
    "voiceId": "string",
    "introMessage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentName` | string | yes | (Required) Name of the agent |
| `introductionAndObjective` | string | yes | (Required) Introduction and objective of the agent |
| `responseGuidelines` | string | yes | (Required) Guidelines for how the agent should respond |
| `task` | string | yes | (Required) The task the agent should perform |
| `faq` | string | no | (Optional) FAQ content for the agent |
| `sampleConversations` | string | no | (Optional) Example conversations for the agent. Use \n for newlines between turns. |
| `primaryLanguage` | string | yes | (Required) Primary language locale for the agent |
| `secondaryLanguage` | string | no | (Optional) Secondary language locale for the agent |
| `voiceId` | string | yes | (Required) Internal AgentVoice ID (UUID). Get available voices from the Get Assistant Voices endpoint. |
| `introMessage` | string | yes | (Required) Introduction message the agent will speak when the call starts |
| `agentType` | string | no | (Required) Type of agent. Defaults to outbound. |
| `customVariables[]` | array<string> | no | (Optional) Custom variables for the agent. For outbound agents, callee_name and mobile_number are always included automatically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
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
| `data.createdAt` | date |  |
| `data.id` | string | The unique ID of the created agent |
| `data.version` | string | The version slug of the agent |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /public/agent` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-agent.md) for the provider-specific parameters and requirements.

