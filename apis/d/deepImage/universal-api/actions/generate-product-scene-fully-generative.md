# DeepImage: Generate Product Scene (Fully Generative)

Creates a fully generative product scene in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-fully-generative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-fully-generative" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://deep-image.ai/api-example.png",
  "background.generate.description": "Item positioned on a moss-covered rock, misty forest in the background."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/generate-product-scene-fully-generative', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://deep-image.ai/api-example.png",
    "background.generate.description": "Item positioned on a moss-covered rock, misty forest in the background."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the product image to integrate into the generated scene. Example: `https://deep-image.ai/api-example.png`. |
| `background.generate.description` | string | yes | Prompt describing the fully generated scene. Example: `Item positioned on a moss-covered rock, misty forest in the background.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background.generate.model_type` | string | no | Generative model used for the scene. Default: `qwen`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-product-scene-fully-generative.md) for the provider-specific parameters and requirements.

