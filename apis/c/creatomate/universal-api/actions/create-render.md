# Creatomate: Create Render

Creates a new render in Creatomate.

```
POST https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/create-render
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/create-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/create-render', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | no | The ID of the template to render. Example: `0bb2ceb3-50b5-48f0-9fe2-84e6bcba43c0`. |
| `modifications` | object | no | A key-value object of template modifications. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `renderScale` | number | no | The render scale from 0.1 to 10. Default is 1.0. Example: `1`. |
| `maxWidth` | number | no | The maximum output width in pixels. Example: `1280`. |
| `maxHeight` | number | no | The maximum output height in pixels. Example: `720`. |
| `webhookUrl` | string | no | The URL to call when the render completes. Example: `https://example.com/creatomate-webhook`. |
| `metadata` | string | no | Optional metadata string to store with the render. Example: `mindcloud:demo`. |
| `outputFormat` | string | no | The RenderScript output format. Example: `mp4`. |
| `width` | number | no | The output width in pixels for a RenderScript request. Example: `1280`. |
| `height` | number | no | The output height in pixels for a RenderScript request. Example: `720`. |
| `elements` | object<object> | no | The RenderScript elements array. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": 1,
      "error_message": "string",
      "file_size": 1,
      "frame_rate": 1,
      "height": 1,
      "id": "string",
      "metadata": "string",
      "modifications": {},
      "output_format": "string",
      "render_scale": 1,
      "snapshot_url": "https://example.com",
      "status": "string",
      "template_id": "string",
      "template_name": "Ava Chen",
      "template_tags": [
        "string"
      ],
      "url": "https://example.com",
      "webhook_url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | number |  |
| `error_message` | string |  |
| `file_size` | number |  |
| `frame_rate` | number |  |
| `height` | number |  |
| `id` | string |  |
| `metadata` | string |  |
| `modifications` | object |  |
| `output_format` | string |  |
| `render_scale` | number |  |
| `snapshot_url` | string |  |
| `status` | string |  |
| `template_id` | string |  |
| `template_name` | string |  |
| `template_tags` | array<string> |  |
| `url` | string |  |
| `webhook_url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Creatomate API, this operation is `POST /v2/renders` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-render.md) for the provider-specific parameters and requirements.

