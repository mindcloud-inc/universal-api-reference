# Printify: Get Upload

Retrieves an upload from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-upload?connectionId=$CONNECTION_ID&image_id=69d963664abf53269b1252a5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "image_id": "69d963664abf53269b1252a5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-upload?${params}`, {
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
| `image_id` | string | yes | Printify upload image id. Default: `69d963664abf53269b1252a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fileName": "Ava Chen",
      "height": 1,
      "id": "string",
      "mimeType": "string",
      "previewUrl": "https://example.com",
      "uploadTime": "string",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fileName` | string |  |
| `height` | number |  |
| `id` | string |  |
| `mimeType` | string |  |
| `previewUrl` | string |  |
| `uploadTime` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Printify API, this operation is `GET /uploads/:image_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload.md) for the provider-specific parameters and requirements.

