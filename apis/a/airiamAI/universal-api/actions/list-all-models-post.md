# Airiam AI: List All Models With Body

Retrieves all active models from Airiam AI by model IDs.

```
GET https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-all-models-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airiam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-all-models-post?connectionId=$CONNECTION_ID&baseModels%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "baseModels[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airiamAI/latest/actions/list-all-models-post?${params}`, {
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
| `baseModels[]` | array<string> | yes | Base model identifiers to include. |

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

Through the native Airiam AI API, this operation is `POST /api/v1/models/list/all` (base URL `https://platform.sectorflow.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-models-post.md) for the provider-specific parameters and requirements.

