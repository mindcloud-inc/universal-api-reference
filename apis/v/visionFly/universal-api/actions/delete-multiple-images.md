# VisionFly: Delete Multiple Images

Deletes multiple images from the VisionFly CDN.

```
DELETE https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-multiple-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VisionFly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-multiple-images?connectionId=$CONNECTION_ID&imageIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/visionFly/latest/actions/delete-multiple-images?${params}`, {
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
| `imageIds[]` | array<string> | yes | Array of VisionFly image identifiers to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": 1,
      "failed": 1,
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | number | Number of deleted images. |
| `failed` | number | Number of images that failed to delete. |
| `results` | array<object> | Per-image delete results. |

## Native endpoint

Through the native VisionFly API, this operation is `DELETE /cdn/images` (base URL `https://api.visionfly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-images.md) for the provider-specific parameters and requirements.

