# Grok: Edit Video

Updates a video in Grok with prompt-based edits.

```
PUT https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string",
  "video": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string",
    "video": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | xAI video editing model. |
| `prompt` | string | yes | Instructions describing the video edit. |
| `video` | object | yes | Source video file or URL to edit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Asynchronous video edit request identifier. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/videos/edits` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-video.md) for the provider-specific parameters and requirements.

