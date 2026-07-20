# Gyazo: Delete Image

Deletes an existing image from Gyazo.

```
DELETE https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/delete-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gyazo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/delete-image?connectionId=$CONNECTION_ID&imageId=8980c52421e452ac3355ca3e5cfe7a0c" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "8980c52421e452ac3355ca3e5cfe7a0c"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gyazo/latest/actions/delete-image?${params}`, {
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
| `imageId` | string | yes | The Gyazo image ID to delete. Example: `8980c52421e452ac3355ca3e5cfe7a0c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "image_id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `image_id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Gyazo API, this operation is `DELETE /api/images/:image_id` (base URL `https://api.gyazo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image.md) for the provider-specific parameters and requirements.

