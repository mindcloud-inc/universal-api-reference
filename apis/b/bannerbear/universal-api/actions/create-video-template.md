# Bannerbear: Create Video Template

Creates a new video template in Bannerbear.

```
POST https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "template": "string",
  "renderType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbear/latest/actions/create-video-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "template": "string",
    "renderType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `template` | string | yes | The existing image template UID to convert into a video template. |
| `renderType` | string | yes | The Bannerbear video build pack to use: overlay, transcribe, or multi_overlay. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `approvalRequired` | boolean | no | Whether manual approval is required before rendering videos from this template. |
| `transcriptionLayerName` | string | no | The text layer name used for transcription output when render_type is transcribe. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannerbear API returns.

## Native endpoint

Through the native Bannerbear API, this operation is `POST /v2/video_templates` (base URL `https://api.bannerbear.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-template.md) for the provider-specific parameters and requirements.

