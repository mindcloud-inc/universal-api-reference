# Runway: Update Avatar

Updates an avatar in Runway.

```
PUT https://connect.mindcloud.co/v1/universal/runway/latest/actions/update-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/runway/latest/actions/update-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/runway/latest/actions/update-avatar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | UUID of the avatar to update. |
| `name` | string | no | Updated avatar name. |
| `personality` | string | no | Updated system prompt for avatar behavior. |
| `referenceImage` | string | no | Updated avatar image URL or data URI. |
| `startScript` | string | no | Optional opening message the avatar says when a session starts. |
| `voice` | object | no | Updated avatar voice object, either runway-live-preset or custom. |

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
      "error": "string",
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
| `error` | string |  |
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

Through the native Runway API, this operation is `PATCH /v1/avatars/[:id]` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-avatar.md) for the provider-specific parameters and requirements.

