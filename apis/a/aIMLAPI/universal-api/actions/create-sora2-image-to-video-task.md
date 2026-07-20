# AI/ML API: Create Sora 2 Image To Video Task

Creates a Sora 2 image-to-video task in AI/ML API.

```
POST https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-sora2-image-to-video-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI/ML API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-sora2-image-to-video-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/create-sora2-image-to-video-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes |  |
| `prompt` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `aspectRatio` | string | no | Default: `16:9`. |
| `duration` | number | no | Default: `4`. |
| `resolution` | string | no | Default: `720p`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AI/ML API API returns.

## Native endpoint

Through the native AI/ML API API, this operation is `POST /v2/video/generations` (base URL `https://api.aimlapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sora2-image-to-video-task.md) for the provider-specific parameters and requirements.

