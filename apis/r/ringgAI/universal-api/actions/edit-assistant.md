# Ringg AI: Edit Assistant

Updates an existing assistant in Ringg AI.

```
PUT https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-assistant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "operation": "string",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/edit-assistant', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "operation": "string",
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `operation` | string | yes |  |
| `agentId` | string | yes |  |
| `agentDisplayName` | string | no |  |
| `language` | string | no |  |
| `voiceId` | string | no |  |
| `secondaryVoiceId` | string | no |  |
| `secondaryLanguage` | string | no |  |
| `agentPrompt` | string | no |  |
| `customVariables[]` | array<string> | no |  |
| `numberId` | string | no |  |
| `kbId` | string | no |  |
| `whitelistedDomains[]` | array<string> | no |  |
| `voiceSpeed` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `message` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `PATCH /agent/v1` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-assistant.md) for the provider-specific parameters and requirements.

