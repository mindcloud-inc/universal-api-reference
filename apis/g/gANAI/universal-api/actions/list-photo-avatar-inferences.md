# GAN.AI: List Photo Avatar Inferences

Retrieves photo avatar inferences from your GAN.AI account.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatar-inferences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatar-inferences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-photo-avatar-inferences?${params}`, {
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
| `photoAvatarId` | string | no |  |
| `startDatetime` | string | no |  |
| `status` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inferenceList": [
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
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inferenceList[].createdAt` | date |  |
| `inferenceList[].creditDetails.ganCost` | number |  |
| `inferenceList[].creditDetails.ttsCost` | number |  |
| `inferenceList[].downloadableVideoLink` | string |  |
| `inferenceList[].inputText` | string |  |
| `inferenceList[].photoAvatarId` | string |  |
| `inferenceList[].photoAvatarInferenceId` | string |  |
| `inferenceList[].status` | string |  |
| `inferenceList[].title` | string |  |
| `inferenceList[].video` | string |  |
| `total` | number |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/photo_avatars/list_inference` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-photo-avatar-inferences.md) for the provider-specific parameters and requirements.

