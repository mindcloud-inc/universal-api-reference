# DeepImage: Prompt-Based Image Editing

Creates an edited image from a prompt in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/prompt-based-image-editing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/prompt-based-image-editing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "background.generate.description": "remove a blue car",
  "background.generate.context_images[0]": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/gitbook1.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/prompt-based-image-editing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "background.generate.description": "remove a blue car",
    "background.generate.context_images[0]": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/gitbook1.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.description` | string | yes | Text prompt describing the edit you want to apply. Example: `remove a blue car`. |
| `background.generate.context_images[0]` | string | yes | Public URL of the source image used as context for the edit. Example: `https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/gitbook1.jpg`. |
| `width` | number | no | Target width of the output image. Default: `1344`. |
| `height` | number | no | Target height of the output image. Default: `768`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/prompt-based-image-editing.md) for the provider-specific parameters and requirements.

