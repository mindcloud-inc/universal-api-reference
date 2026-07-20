# DeepImage: Generate Product Scene (Blended)

Creates a blended product scene in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-blended
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-blended" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example.png",
  "background.generate.description": "Small item positioned on a moss-covered rock, misty forest in the background."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-blended', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example.png",
    "background.generate.description": "Small item positioned on a moss-covered rock, misty forest in the background."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the product image to place into the generated scene. Example: `https://deep-image.ai/api-example.png`. |
| `background.generate.description` | string | yes | Prompt describing the target scene around the product. Example: `Small item positioned on a moss-covered rock, misty forest in the background.`. |
| `background.generate.item_area_percentage` | number | no | Value between 0 and 1 controlling how much of the image the product should occupy. Default: `0.75`. |
| `width` | number | no | Optional output width in pixels. Default: `1000`. |
| `height` | number | no | Optional output height in pixels. Default: `1000`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-product-scene-blended.md) for the provider-specific parameters and requirements.

