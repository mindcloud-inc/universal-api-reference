# GAN.AI: List Avatar Videos

Retrieves avatar videos from your GAN.AI account.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatar-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatar-videos?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatar-videos?${params}`, {
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
| `avatarId` | string | no |  |
| `avatarTitle` | string | no |  |
| `endDatetime` | string | no |  |
| `inferenceTitle` | string | no |  |
| `startDatetime` | string | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarId": "string",
      "avatarTitle": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "inferenceId": "string",
      "inputText": "string",
      "status": "string",
      "thumbnail": "string",
      "title": "string",
      "video": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarId` | string | Avatar identifier. |
| `avatarTitle` | string | Avatar title. |
| `createdAt` | date | Creation timestamp. |
| `inferenceId` | string | Inference identifier. |
| `inputText` | string | Source input text. |
| `status` | string | Inference status. |
| `thumbnail` | string | Thumbnail URL. |
| `title` | string | Inference title. |
| `video` | string | Generated video URL. |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/avatars/list_inferences` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-avatar-videos.md) for the provider-specific parameters and requirements.

