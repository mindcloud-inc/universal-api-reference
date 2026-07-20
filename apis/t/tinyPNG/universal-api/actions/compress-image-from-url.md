# TinyPNG: Compress Image From URL

Compresses an image from a URL with TinyPNG.

```
POST https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/compress-image-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TinyPNG `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/compress-image-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://tinypng.com/images/panda-happy.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinyPNG/latest/actions/compress-image-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://tinypng.com/images/panda-happy.png"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Public URL of the image to optimize with TinyPNG. Example: `https://tinypng.com/images/panda-happy.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "input": {
        "size": 1,
        "type": "string"
      },
      "output": {
        "height": 1,
        "ratio": 1,
        "size": 1,
        "type": "string",
        "url": "https://example.com",
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `input.size` | number |  |
| `input.type` | string |  |
| `output.height` | number |  |
| `output.ratio` | number |  |
| `output.size` | number |  |
| `output.type` | string |  |
| `output.url` | string |  |
| `output.width` | number |  |

## Native endpoint

Through the native TinyPNG API, this operation is `POST /shrink` (base URL `https://api.tinify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compress-image-from-url.md) for the provider-specific parameters and requirements.

