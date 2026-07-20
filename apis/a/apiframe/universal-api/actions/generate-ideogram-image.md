# Apiframe: Generate Ideogram Image

Creates an Ideogram image generation task in Apiframe.

```
POST https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/generate-ideogram-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/generate-ideogram-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/generate-ideogram-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `prompt` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image_urls": [
        "https://example.com"
      ],
      "seed": 1,
      "status": "string",
      "task_id": "string",
      "task_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image_urls` | array<string> |  |
| `seed` | number |  |
| `status` | string |  |
| `task_id` | string |  |
| `task_type` | string |  |

## Native endpoint

Through the native Apiframe API, this operation is `POST /ideogram-imagine` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ideogram-image.md) for the provider-specific parameters and requirements.

