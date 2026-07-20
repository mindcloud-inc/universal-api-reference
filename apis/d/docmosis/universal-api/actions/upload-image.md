# Docmosis: Upload Image



```
POST https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageFile": "Upload a PNG, JPG, or GIF image"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageFile": "Upload a PNG, JPG, or GIF image"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageFile` | file | yes | Image file stream to upload. Example: `Upload a PNG, JPG, or GIF image`. |
| `imageName` | string | no | Override name and optional folder path for the uploaded image. Example: `stage3/docmosis/20260325t134628/images/logo.png`. |
| `imageDescription` | string | no | Short description for the uploaded image. Example: `MindCloud stage 3 test image`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `normalizeImageName` | boolean | no | Normalize the uploaded image name using Unicode NFC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageDetails": {},
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageDetails` | object | Stored image metadata returned by Docmosis. |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the image upload succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /uploadImage` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image.md) for the provider-specific parameters and requirements.

