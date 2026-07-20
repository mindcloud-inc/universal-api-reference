# Grok: Generate Image

Creates images from prompts in Grok.

```
POST https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/generate-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | xAI image generation model. |
| `prompt` | string | yes | Text prompt describing the image to generate. |
| `n` | number | no | Number of images to generate. |
| `aspectRatio` | string | no | Desired output aspect ratio. |
| `resolution` | string | no | Desired output resolution. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "b64Json": "string",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Generated images returned by xAI. |
| `data[].b64Json` | string | Base64-encoded image payload when base64 output is requested. |
| `data[].url` | string | Hosted image URL when URL output is requested. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/images/generations` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image.md) for the provider-specific parameters and requirements.

