# GAN.AI: List Photo Avatars

Retrieves photo avatars from your GAN.AI account.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatars?${params}`, {
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
| `endDatetime` | string | no |  |
| `startDatetime` | string | no |  |
| `status` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarsList": [
        {
          "baseImage": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "photoAvatarId": "string",
          "status": "string",
          "title": "string"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarsList[].baseImage` | string |  |
| `avatarsList[].createdAt` | date |  |
| `avatarsList[].photoAvatarId` | string |  |
| `avatarsList[].status` | string |  |
| `avatarsList[].title` | string |  |
| `total` | number |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/photo_avatars/list` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-photo-avatars.md) for the provider-specific parameters and requirements.

