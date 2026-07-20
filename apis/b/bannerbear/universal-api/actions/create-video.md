# Bannerbear: Create Video

Creates a new video in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoTemplate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoTemplate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoTemplate` | string | yes | The Bannerbear video template UID. |
| `inputMediaUrl` | string | no | Input media URL for dynamic video scenes when required by the template. |
| `modifications` | list<object> | no | Layer modifications to apply when generating the video. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `zoom` | string | no | Zoom mode for the generated video. |
| `zoomFactor` | number | no | Zoom factor for the generated video. |
| `blur` | number | no | Blur amount for the generated video. |
| `trimStartTime` | string | no | Start time for trimming the input media. |
| `trimEndTime` | string | no | End time for trimming the input media. |
| `trimToLengthInSeconds` | number | no | Trim the input media to a target duration in seconds. |
| `webhookUrl` | string | no | Webhook URL to receive the render result. |
| `metadata` | string | no | Custom metadata to attach to the generated video. |
| `frames` | list<object> | no | Per-frame layer data for animated scenes when supported. |
| `frameDurations` | list<number> | no | Frame durations for animated video scenes. |
| `createGifPreview` | boolean | no | Create a GIF preview for the generated video. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/videos` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video.md) for the provider-specific parameters and requirements.

