# DeepImage: Auto Enhance Generative

Creates a generatively enhanced image in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/auto-enhance-generative
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/auto-enhance-generative" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/old_photo.jpeg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/auto-enhance-generative', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/old_photo.jpeg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Public URL of the image to auto enhance. Example: `https://s3.eu-central-1.amazonaws.com/deep-image.ai/api-examples/old_photo.jpeg`. |

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
| `imageApp` | string | Image app identifier returned by DeepImage when present. |
| `job` | string | DeepImage processing job hash. |
| `originalImg` | string | DeepImage copy of the original input image when present. |
| `queue` | number | Queue position returned by DeepImage when present. |

## Native endpoint

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-enhance-generative.md) for the provider-specific parameters and requirements.

