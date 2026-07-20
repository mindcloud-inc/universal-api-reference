# Reka Vision: Delete Video By Id (V1)

Deletes a video from Reka Vision by ID.

```
DELETE https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/delete-video-by-id-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/delete-video-by-id-v1?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/delete-video-by-id-v1?${params}`, {
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
| `videoId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Status message |
| `status` | string | Status of the deletion |

## Native endpoint

Through the native Reka Vision API, this operation is `DELETE /v1/videos/:videoId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-video-by-id-v1.md) for the provider-specific parameters and requirements.

