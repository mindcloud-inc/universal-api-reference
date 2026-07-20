# CustomGPT.ai: Get Agent Settings

Retrieves current agent settings from CustomGPT.ai.

```
GET https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomGPT.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-settings?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customGPTai/latest/actions/get-agent-settings?${params}`, {
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
| `projectId` | number | yes | The project ID of the agent to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentCapability": "string",
      "canExportConversation": true,
      "canShareConversation": true,
      "chatbotModel": "string",
      "chatbotMsgLang": "string",
      "defaultPrompt": "string",
      "enableCitations": 1,
      "exampleQuestions": [
        "string"
      ],
      "markdownEnabled": true,
      "personaInstructions": "string",
      "removeBranding": true,
      "responseSource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentCapability` | string |  |
| `canExportConversation` | boolean |  |
| `canShareConversation` | boolean |  |
| `chatbotModel` | string |  |
| `chatbotMsgLang` | string |  |
| `defaultPrompt` | string |  |
| `enableCitations` | number |  |
| `exampleQuestions` | array<string> |  |
| `markdownEnabled` | boolean |  |
| `personaInstructions` | string |  |
| `removeBranding` | boolean |  |
| `responseSource` | string |  |

## Native endpoint

Through the native CustomGPT.ai API, this operation is `GET /projects/:projectId/settings` (base URL `https://app.customgpt.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-settings.md) for the provider-specific parameters and requirements.

