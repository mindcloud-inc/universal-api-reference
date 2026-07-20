# Bannerbite: Generate Image Or Video

Creates an image or video render job in Bannerbite.

```
POST https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/generate-image-or-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannerbite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/generate-image-or-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sceneData": {},
  "type": "image",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannerbite/latest/actions/generate-image-or-video', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sceneData": {},
    "type": "image",
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | no | Optional email address that receives the finished render. |
| `scene` | number | no | Required when type is image. Selects which scene to render. Default: `1`. |
| `sceneData` | list<object> | yes | Array of scene variable objects to inject into the selected bite. Send each object with provider keys such as name, value, color, width, height, inPoint, outPoint, visibility, and position when applicable. |
| `type` | string | yes | Render type. Bannerbite documents image, video, and overlay. One of: `0`, `1`, `2`. Default: `image`. |
| `uid` | string | yes | The bite ID or bite access token used for the render request. |
| `webhook` | string | no | Optional webhook URL for render status notifications. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audio` | object | no | Optional audio object containing url and inPoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Bannerbite API, this operation is `POST /api/render` (base URL `https://api.bannerbite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-or-video.md) for the provider-specific parameters and requirements.

