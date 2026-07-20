# DeepImage: Storage-to-Storage Processing

Queues storage-to-storage image processing in DeepImage.

```
POST https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/storage-to-storage-processing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeepImage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/storage-to-storage-processing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "storage://aws-deep-image/2025/may/my-photo.png",
  "target": "storage://onedrive-deep-image/processed"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepImage/latest/actions/storage-to-storage-processing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "storage://aws-deep-image/2025/may/my-photo.png",
    "target": "storage://onedrive-deep-image/processed"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | DeepImage storage URL of the source image, for example `storage://aws-deep-image/2025/may/my-photo.png`. Example: `storage://aws-deep-image/2025/may/my-photo.png`. |
| `target` | string | yes | DeepImage storage URL where the processed result should be written. Example: `storage://onedrive-deep-image/processed`. |

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

Through the native DeepImage API, this operation is `POST /rest_api/process` (base URL `https://deep-image.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/storage-to-storage-processing.md) for the provider-specific parameters and requirements.

