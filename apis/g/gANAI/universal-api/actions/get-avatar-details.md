# GAN.AI: Get Avatar Details

Retrieves details for an avatar in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-details?connectionId=$CONNECTION_ID&avatarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "avatarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-avatar-details?${params}`, {
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
| `avatarId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarId": "string",
      "avatarMetadata": {
        "avatarType": "string",
        "frameBoundingBoxesS3Key": "string",
        "isSoraGen": true,
        "maximalBoundingBox": "string",
        "sourceAvatarId": "string",
        "thumbnailDimension": "string",
        "videoDimension": "string"
      },
      "avatarType": "string",
      "avatarVerificationFailureMetadata": "string",
      "backendCheckResults": "string",
      "baseVideo": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "maximalBoundingBox": "string",
      "status": "string",
      "thumbnail": "string",
      "thumbnails": {
        "defaultAlphaMask": "string",
        "defaultBasic": "string",
        "defaultNoBg": "string",
        "landscapeAlphaMask": "string",
        "landscapeBasic": "string",
        "landscapeNoBg": "string",
        "portraitAlphaMask": "string",
        "portraitBasic": "string",
        "portraitNoBg": "string"
      },
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
| `avatarMetadata.avatarType` | string |  |
| `avatarMetadata.frameBoundingBoxesS3Key` | string |  |
| `avatarMetadata.isSoraGen` | boolean |  |
| `avatarMetadata.maximalBoundingBox` | string |  |
| `avatarMetadata.sourceAvatarId` | string |  |
| `avatarMetadata.thumbnailDimension` | string |  |
| `avatarMetadata.videoDimension` | string |  |
| `avatarType` | string |  |
| `avatarVerificationFailureMetadata` | string |  |
| `backendCheckResults` | string |  |
| `baseVideo` | string |  |
| `createdAt` | date |  |
| `maximalBoundingBox` | string |  |
| `status` | string |  |
| `thumbnail` | string |  |
| `thumbnails.defaultAlphaMask` | string |  |
| `thumbnails.defaultBasic` | string |  |
| `thumbnails.defaultNoBg` | string |  |
| `thumbnails.landscapeAlphaMask` | string |  |
| `thumbnails.landscapeBasic` | string |  |
| `thumbnails.landscapeNoBg` | string |  |
| `thumbnails.portraitAlphaMask` | string |  |
| `thumbnails.portraitBasic` | string |  |
| `thumbnails.portraitNoBg` | string |  |
| `title` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/avatars/avatar_details` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-avatar-details.md) for the provider-specific parameters and requirements.

