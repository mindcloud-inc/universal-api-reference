# Reka Vision: Upload Images (V1)

Uploads images to Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-images-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-images-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "metadata": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/upload-images-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "metadata": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `images[]` | array<file> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageId": "string",
      "imageUrl": "https://example.com",
      "indexingStatus": 1,
      "uploadTimestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageId` | string |  |
| `imageUrl` | string |  |
| `indexingStatus` | number |  |
| `uploadTimestamp` | number |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v1/images/upload` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-images-v1.md) for the provider-specific parameters and requirements.

