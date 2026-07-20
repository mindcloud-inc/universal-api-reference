# Airiam AI: Get All Models

Retrieves all models from Airiam AI.

```
GET https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-all-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-all-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/get-all-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
| `active` | boolean | Whether the model is active. |
| `baseModel` | string | Provider base model identifier used by detail endpoints. |
| `chatCredits` | number | Chat credit cost. |
| `contextWindow` | number | Model context window size. |
| `created` | date | Model creation timestamp. |
| `description` | string | Model description. |
| `hasVision` | boolean | Whether the model supports vision input. |
| `icon` | string | Model provider icon key. |
| `id` | string | Model UUID. |
| `imageGen` | boolean | Whether the model generates images. |
| `instructionFollowing` | boolean | Whether instruction following is enabled. |
| `internalUseOnly` | boolean | Whether the model is internal only. |
| `maxCompletionTokens` | number | Maximum completion tokens when provided. |
| `modelRating` | number | Airiam model rating. |
| `name` | string | Model display name. |
| `pdfVision` | boolean | Whether the model supports PDF vision. |
| `promptWrapper` | object | Prompt wrapper metadata. |
| `settingsAvailable` | array<object> | Configurable model settings. |
| `updated` | date | Model update timestamp. |
| `usesSystemPrompts` | boolean | Whether the model supports system prompts. |

## Native endpoint

Through the native Airiam AI API, this operation is `GET /api/v1/models/all` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-all-models.md) for the provider-specific parameters and requirements.

