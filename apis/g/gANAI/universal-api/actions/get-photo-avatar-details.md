# GAN.AI: Get Photo Avatar Details

Retrieves details for a photo avatar in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-details?connectionId=$CONNECTION_ID&photoAvatarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "photoAvatarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-details?${params}`, {
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
| `photoAvatarId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseImage": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "photoAvatarId": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseImage` | string |  |
| `createdAt` | date |  |
| `photoAvatarId` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/photo_avatars/details` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photo-avatar-details.md) for the provider-specific parameters and requirements.

