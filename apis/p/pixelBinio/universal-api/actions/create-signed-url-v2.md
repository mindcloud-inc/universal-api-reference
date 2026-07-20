# PixelBin.io: Create Signed URL V2

Creates a new signed multipart upload URL in PixelBin.io.

```
POST https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "access": "private",
  "expiry": "300",
  "format": "string",
  "name": "Ava Chen",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/create-signed-url-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "access": "private",
    "expiry": "300",
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
| `expiry` | number | yes | Default: `300`. |
| `format` | string | yes |  |
| `name` | string | yes |  |
| `path` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "presignedUrl": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `presignedUrl` | object | Multipart signed upload payload. |

## Native endpoint

Through the native PixelBin.io API, this operation is `POST /service/platform/assets/v2.0/upload/signed-url` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-signed-url-v2.md) for the provider-specific parameters and requirements.

