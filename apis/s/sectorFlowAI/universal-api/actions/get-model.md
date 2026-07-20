# SectorFlow.AI: Get Model



```
GET https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-model?connectionId=$CONNECTION_ID&modelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "modelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-model?${params}`, {
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
| `modelId` | string | yes | The model UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "baseModel": "string",
      "chatCredits": 1,
      "contextWindow": 1,
      "created": "string",
      "description": "string",
      "hasVision": true,
      "icon": "string",
      "id": "string",
      "imageGen": true,
      "instructionFollowing": true,
      "internalUseOnly": true,
      "maxCompletionTokens": 1,
      "modelRating": 1,
      "name": "Ava Chen",
      "pdfVision": true,
      "promptWrapper": {},
      "settingsAvailable": [
        {}
      ],
      "updated": "string",
      "usesSystemPrompts": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `baseModel` | string |  |
| `chatCredits` | number |  |
| `contextWindow` | number |  |
| `created` | string |  |
| `description` | string |  |
| `hasVision` | boolean |  |
| `icon` | string |  |
| `id` | string |  |
| `imageGen` | boolean |  |
| `instructionFollowing` | boolean |  |
| `internalUseOnly` | boolean |  |
| `maxCompletionTokens` | number |  |
| `modelRating` | number |  |
| `name` | string |  |
| `pdfVision` | boolean |  |
| `promptWrapper` | object |  |
| `settingsAvailable` | array<object> |  |
| `updated` | string |  |
| `usesSystemPrompts` | boolean |  |

## Native endpoint

Through the native SectorFlow.AI API, this operation is `GET /models/{modelId}` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model.md) for the provider-specific parameters and requirements.

