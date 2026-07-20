# VisionFly: Delete Image from CDN

Deletes an image from the VisionFly CDN.

```
DELETE https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-image-from-cdn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-image-from-cdn?connectionId=$CONNECTION_ID&imageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-image-from-cdn?${params}`, {
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
| `imageId` | string | yes | VisionFly image identifier to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageId` | string | Deleted image identifier. |
| `success` | boolean | Whether the delete operation succeeded. |

## Native endpoint

Through the native VisionFly API, this operation is `DELETE /cdn/:image_id` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image-from-cdn.md) for the provider-specific parameters and requirements.

