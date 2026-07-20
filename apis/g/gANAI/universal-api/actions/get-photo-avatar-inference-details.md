# GAN.AI: Get Photo Avatar Inference Details

Retrieves details for a photo avatar inference in GAN.AI.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-inference-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-inference-details?connectionId=$CONNECTION_ID&photoAvatarInferenceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "photoAvatarInferenceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/get-photo-avatar-inference-details?${params}`, {
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
| `downloadableLink` | boolean | no |  |
| `photoAvatarInferenceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditDetails": {
        "ganCost": 1,
        "ttsCost": 1
      },
      "downloadableVideoLink": "https://example.com",
      "inputText": "string",
      "photoAvatarId": "string",
      "photoAvatarInferenceId": "string",
      "status": "string",
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
| `createdAt` | date |  |
| `creditDetails.ganCost` | number |  |
| `creditDetails.ttsCost` | number |  |
| `downloadableVideoLink` | string |  |
| `inputText` | string |  |
| `photoAvatarId` | string |  |
| `photoAvatarInferenceId` | string |  |
| `status` | string |  |
| `title` | string |  |
| `video` | string |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/photo_avatars/inference_details` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photo-avatar-inference-details.md) for the provider-specific parameters and requirements.

