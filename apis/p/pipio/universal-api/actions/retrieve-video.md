# Pipio: Retrieve Video

Retrieves a generated video from Pipio.

```
GET https://connect.mindcloud.co/v1/universal/pipio/latest/actions/retrieve-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipio/latest/actions/retrieve-video?connectionId=$CONNECTION_ID&id=61de44f6ef604e048a8b4f887d9ef426" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "61de44f6ef604e048a8b4f887d9ef426"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipio/latest/actions/retrieve-video?${params}`, {
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
| `id` | string | yes | The unique identifier for your video. Example: `61de44f6ef604e048a8b4f887d9ef426`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "actorId": "string",
      "aspectRatio": 1,
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creditCost": 1,
      "estimatedCompleteDate": "2026-05-07T12:00:00.000Z",
      "fps": 1,
      "id": "string",
      "language": "string",
      "processingStatus": "string",
      "script": "string",
      "status": "string",
      "transparent": true,
      "videoUrl": "https://example.com",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string | Account id. |
| `actorId` | string | Actor id. |
| `aspectRatio` | number | Aspect ratio. |
| `createdDate` | date | Creation time. |
| `creditCost` | number | Credit cost. |
| `estimatedCompleteDate` | date | Estimated completion time. |
| `fps` | number | Frame rate. |
| `id` | string | Video id. |
| `language` | string | Video language. |
| `processingStatus` | string | Detailed processing status. |
| `script` | string | Video script. |
| `status` | string | Video status. |
| `transparent` | boolean | Transparent background flag. |
| `videoUrl` | string | Completed video URL. |
| `voiceId` | string | Voice id. |

## Native endpoint

Through the native Pipio API, this operation is `GET https://generate.pipio.ai/single-clip/:id` (base URL `https://avatar.pipio.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-video.md) for the provider-specific parameters and requirements.

