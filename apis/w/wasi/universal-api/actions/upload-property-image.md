# Wasi: Upload Property Image

Uploads a property image to Wasi.

```
POST https://connect.mindcloud.co/v1/universal/wasi/latest/actions/upload-property-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/upload-property-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property_id": "1",
  "image_file": "https://example.com/test.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/upload-property-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property_id": "1",
    "image_file": "https://example.com/test.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `property_id` | number | yes | Wasi property ID. Default: `1`. |
| `image_file` | string | yes | Image file payload placeholder for Wasi multipart upload scaffolding. Default: `https://example.com/test.jpg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id_image": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id_image` | number | Uploaded image identifier when Wasi returns it. |
| `status` | string | Wasi operation status. |

## Native endpoint

Through the native Wasi API, this operation is `POST /property/upload-image/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-property-image.md) for the provider-specific parameters and requirements.

