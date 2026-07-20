# Uniqode: Download QR Code Image

Retrieves QR code image download URLs from Uniqode.

```
GET https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/download-qr-code-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/download-qr-code-image?connectionId=$CONNECTION_ID&qrCodeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCodeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/download-qr-code-image?${params}`, {
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
| `qrCodeId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "urls": {
        "png": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `urls` | object |  |
| `urls.png` | string |  |

## Native endpoint

Through the native Uniqode API, this operation is `GET /qrcodes/:qrCodeId/download/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-qr-code-image.md) for the provider-specific parameters and requirements.

