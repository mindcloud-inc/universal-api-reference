# GAN.AI: Create Avatar

Creates an avatar in GAN.AI.

```
POST https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseVideoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/create-avatar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseVideoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseVideoUrl` | string | yes |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarId": "string",
      "avatarType": "string",
      "baseVideo": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "estimatedCompletionTime": 1,
      "status": "string",
      "thumbnail": "string",
      "thumbnails": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarId` | string |  |
| `avatarType` | string |  |
| `baseVideo` | string |  |
| `createdAt` | date |  |
| `estimatedCompletionTime` | number |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `thumbnails` | string |  |
| `title` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `POST /v1/avatars/create_avatar` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-avatar.md) for the provider-specific parameters and requirements.

