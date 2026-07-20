# Phonely: Update Agent

Updates an agent in Phonely.

```
PUT https://connect.mindcloud.co/v1/universal/phonely/latest/actions/update-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/update-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
  "agentId": "new-agent-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/update-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
    "agentId": "new-agent-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Your Phonely user ID. Example: `W4LT4yDethRPfyCn9YAEVeIqrDf1`. |
| `agentId` | string | yes | The ID of the agent to update. Example: `new-agent-id`. |
| `agentName` | string | no | New name for the agent. Maximum 50 characters. Example: `MindCloud Test Agent`. |
| `greetingMessage` | string | no | New greeting message. Maximum 500 characters. Example: `Hello! How can I help you today?`. |
| `conversationStyle` | string | no | Conversation style. Use one of: Casual, Humorous, Direct, Formal, Persuasive, Friendly. Example: `Friendly`. |
| `humanizeConversation` | boolean | no | Whether to humanize the conversation. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `voiceId` | string | no | ID of the voice to use for the agent. Example: `voice-id`. |
| `orgId` | string | no | Organization ID to move the agent to. Example: `org-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/update-agent` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent.md) for the provider-specific parameters and requirements.

