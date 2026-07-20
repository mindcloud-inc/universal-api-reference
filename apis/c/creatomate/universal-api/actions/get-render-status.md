# Creatomate: Get Render Status

Retrieves a render's status from Creatomate.

```
GET https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Creatomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status?connectionId=$CONNECTION_ID&renderId=c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/creatomate/latest/actions/get-render-status?${params}`, {
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
| `renderId` | string | yes | The ID of the render to retrieve. Example: `c4f6d4f1-7a4e-4b67-9f90-3fc76f3c7d0e`. |

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

Through the native Creatomate API, this operation is `GET /v2/renders/:render_id` (base URL `https://api.creatomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-render-status.md) for the provider-specific parameters and requirements.

