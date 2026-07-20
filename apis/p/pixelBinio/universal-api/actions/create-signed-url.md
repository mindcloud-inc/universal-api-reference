# PixelBin.io: Create Signed URL

Creates a new signed upload URL in PixelBin.io.

```
POST https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "access": "private",
  "format": "string",
  "name": "Ava Chen",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "access": "private",
    "format": "string",
    "name": "Ava Chen",
    "path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `access` | string | yes | Default: `private`. |
| `format` | string | yes |  |
| `name` | string | yes |  |
| `path` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "s3PresignedUrl": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `s3PresignedUrl` | object | Single-part signed upload payload. |

## Native endpoint

Through the native PixelBin.io API, this operation is `POST /service/platform/assets/v1.0/upload/signed-url` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signed-url.md) for the provider-specific parameters and requirements.

