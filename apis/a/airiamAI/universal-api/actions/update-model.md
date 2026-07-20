# Airiam AI: Update Model

Updates an existing model in Airiam AI.

```
PUT https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/update-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelId` | string | yes | Model UUID. |
| `name` | string | no | Updated model display name. |

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
      "created": "2026-05-07T12:00:00.000Z",
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
      "updated": "2026-05-07T12:00:00.000Z",
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
| `created` | date |  |
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
| `updated` | date |  |
| `usesSystemPrompts` | boolean |  |

## Native endpoint

Through the native Airiam AI API, this operation is `PATCH /api/v1/models/:modelId` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model.md) for the provider-specific parameters and requirements.

