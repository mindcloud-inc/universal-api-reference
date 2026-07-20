# Runway: Get Avatar

Retrieves an avatar from Runway.

```
GET https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-avatar?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runway/latest/actions/get-avatar?${params}`, {
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
| `id` | string | yes | UUID of the avatar to retrieve. |

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

Through the native Runway API, this operation is `GET /v1/avatars/[:id]` (base URL `https://api.dev.runwayml.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar.md) for the provider-specific parameters and requirements.

