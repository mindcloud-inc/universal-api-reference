# CustomGPT.ai: Update Agent Settings

Updates current agent settings in CustomGPT.ai.

```
PUT https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/update-agent-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes | The project ID of the agent. |
| `defaultPrompt` | string | no | The default prompt shown for the agent. |
| `responseSource` | string | no | How the agent should cite or source responses. |
| `chatbotMessageLanguage` | string | no | The language code used for chatbot UI messages. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatbotMsgLang": "string",
      "defaultPrompt": "string",
      "exampleQuestions": [
        "string"
      ],
      "removeBranding": true,
      "responseSource": "string",
      "updated": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatbotMsgLang` | string |  |
| `defaultPrompt` | string |  |
| `exampleQuestions` | array<string> |  |
| `removeBranding` | boolean |  |
| `responseSource` | string |  |
| `updated` | boolean |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `POST /projects/:projectId/settings` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent-settings.md) for the provider-specific parameters and requirements.

