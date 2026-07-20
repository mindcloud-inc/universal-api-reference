# Reka Vision: Get Image By Id (V1)

Retrieves an image from Reka Vision by ID.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-image-by-id-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-image-by-id-v1?connectionId=$CONNECTION_ID&imageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-image-by-id-v1?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageId` | string | yes |  |

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

Through the native Reka Vision API, this operation is `GET /v1/images/:imageId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-by-id-v1.md) for the provider-specific parameters and requirements.

