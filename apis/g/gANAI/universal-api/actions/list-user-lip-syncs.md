# GAN.AI: List User LipSyncs

Retrieves lip-sync videos from your GAN.AI account.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-user-lip-syncs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-user-lip-syncs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-user-lip-syncs?${params}`, {
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
      "lipsyncs": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "inferenceId": "string",
          "inputAudio": "string",
          "inputVideo": "string",
          "status": "string",
          "thumbnailUrl": "https://example.com",
          "title": "string",
          "useAudioFromVideo": true,
          "videoUrl": "https://example.com"
        }
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lipsyncs[].createdAt` | date | Creation timestamp. |
| `lipsyncs[].description` | string | Lip sync description. |
| `lipsyncs[].inferenceId` | string | Inference identifier. |
| `lipsyncs[].inputAudio` | string | Input audio URL. |
| `lipsyncs[].inputVideo` | string | Input video URL. |
| `lipsyncs[].status` | string | Inference status. |
| `lipsyncs[].thumbnailUrl` | string | Thumbnail URL. |
| `lipsyncs[].title` | string | Lip sync title. |
| `lipsyncs[].useAudioFromVideo` | boolean | Whether source video audio was reused. |
| `lipsyncs[].videoUrl` | string | Generated video URL. |
| `totalCount` | number | Total number of lip sync jobs. |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/lipsync/get_user_lipsyncs` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-lip-syncs.md) for the provider-specific parameters and requirements.

