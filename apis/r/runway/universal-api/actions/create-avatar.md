# Runway: Create Avatar

Creates an avatar in Runway.

```
POST https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "personality": "string",
  "referenceImage": "string",
  "voice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/create-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "personality": "string",
    "referenceImage": "string",
    "voice": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Character name for the avatar. |
| `personality` | string | yes | System prompt describing how the avatar should behave. |
| `referenceImage` | string | yes | HTTPS URL, Runway URI, or data URI for the avatar image. |
| `voice` | object | yes | Voice object for the avatar, either runway-live-preset or custom. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "documentIds": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "personality": "string",
      "processedImageUri": "string",
      "referenceImageUri": "string",
      "startScript": "string",
      "status": "string",
      "updatedAt": "string",
      "voice": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `documentIds` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `personality` | string |  |
| `processedImageUri` | string |  |
| `referenceImageUri` | string |  |
| `startScript` | string |  |
| `status` | string |  |
| `updatedAt` | string |  |
| `voice` | object |  |

## Native endpoint

Through the native Runway API, this operation is `POST /v1/avatars` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-avatar.md) for the provider-specific parameters and requirements.

