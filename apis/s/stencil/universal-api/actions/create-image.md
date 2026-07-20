# Stencil: Create Image



```
POST https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stencil `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stencil/latest/actions/create-image', {
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
| `jpegQuality` | number | no | JPEG quality between 0 and 1. |
| `metadata` | object | no | Extra metadata to include with the result. |
| `modifications[]` | array<object> | no | Array of modification objects. |
| `pngMultiplier` | number | no | PNG quality multiplier. |
| `template` | string | no | Template ID to generate from. |
| `transparent` | boolean | no | Whether the generated image background should be transparent. |
| `webhookUrl` | string | no | Webhook URL called when image processing completes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "imageUrl": "https://example.com",
      "imageUrlJpg": "https://example.com",
      "log": "string",
      "metadata": {},
      "modifications": [
        {}
      ],
      "self": "string",
      "status": "string",
      "templateId": "string",
      "webhookResponseBody": "string",
      "webhookResponseCode": 1,
      "webhookUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `id` | string |  |
| `imageUrl` | string |  |
| `imageUrlJpg` | string |  |
| `log` | string |  |
| `metadata` | object |  |
| `modifications` | array<object> |  |
| `self` | string |  |
| `status` | string |  |
| `templateId` | string |  |
| `webhookResponseBody` | string |  |
| `webhookResponseCode` | number |  |
| `webhookUrl` | string |  |

## Native endpoint

Through the native Stencil API, this operation is `POST /v1/images` (base URL `https://api.usestencil.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-image.md) for the provider-specific parameters and requirements.

