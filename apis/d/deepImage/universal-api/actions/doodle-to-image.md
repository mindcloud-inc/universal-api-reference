# DeepImage: Doodle to Image

Creates an image from a doodle in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/doodle-to-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/doodle-to-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/flowers-6770694_1280.jpg",
  "background.generate.description": "realistic version of flowers in the mountains"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/doodle-to-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/flowers-6770694_1280.jpg",
    "background.generate.description": "realistic version of flowers in the mountains"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the sketch or doodle image to transform. Example: `https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/flowers-6770694_1280.jpg`. |
| `background.generate.description` | string | yes | Prompt describing what the doodle should become. Example: `realistic version of flowers in the mountains`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageApp": "string",
      "job": "string",
      "originalImg": "string",
      "queue": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageApp` | string |  |
| `job` | string |  |
| `originalImg` | string |  |
| `queue` | number |  |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/doodle-to-image.md) for the provider-specific parameters and requirements.

