# Grok: Edit Image

Updates an image in Grok with prompt-based edits.

```
PUT https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string",
  "images[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/edit-image', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string",
    "images[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | string | yes | xAI image editing model. |
| `prompt` | string | yes | Instructions describing the image edit. |
| `images[]` | array<object> | yes | Source images to edit. |

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
| `data` | array<object> | Edited images returned by xAI. |
| `data[].b64Json` | string | Base64-encoded image payload when base64 output is requested. |
| `data[].url` | string | Hosted image URL when URL output is requested. |

## Native endpoint

Through the native Grok API, this operation is `POST /v1/images/edits` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-image.md) for the provider-specific parameters and requirements.

