# PromptLayer Run Agent: Track Prompt

Tracks prompts in PromptLayer.

```
PUT https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/track-prompt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PromptLayer Run Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/track-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "promptName": "Ava Chen",
  "requestId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/promptLayerRunAgent/latest/actions/track-prompt', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "promptName": "Ava Chen",
    "requestId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `promptName` | string | yes | Prompt template name to associate with the request. |
| `requestId` | number | yes | PromptLayer request ID to update. |
| `promptInputVariables` | object | no | Input variables used for the prompt template. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `version` | number | no | Prompt template version number. Mutually exclusive with label. |
| `label` | string | no | Prompt template release label. Mutually exclusive with version. |

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

Through the native PromptLayer Run Agent API, this operation is `POST /rest/track-prompt` (base URL `https://api.promptlayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-prompt.md) for the provider-specific parameters and requirements.

