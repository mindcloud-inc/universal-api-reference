# Apiframe: Remix Ideogram Image

Creates an Ideogram remix task in Apiframe.

```
POST https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/remix-ideogram-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/remix-ideogram-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com",
  "prompt": "string",
  "imageWeight": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/remix-ideogram-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com",
    "prompt": "string",
    "imageWeight": 1
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
| `imageWeight` | number | yes |  |

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

Through the native Apiframe API, this operation is `POST /ideogram-remix` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remix-ideogram-image.md) for the provider-specific parameters and requirements.

