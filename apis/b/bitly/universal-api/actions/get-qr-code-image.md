# Bitly: Get QR Code Image

Retrieves a QR code image from Bitly.

```
GET https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-qr-code-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bitly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-qr-code-image?connectionId=$CONNECTION_ID&qrcodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrcodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitly/latest/actions/get-qr-code-image?${params}`, {
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
| `format` | string | no |  |
| `qrcodeId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "qrCodeImage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `qrCodeImage` | string |  |

## Native endpoint

Through the native Bitly API, this operation is `GET /qr-codes/:qrcode_id/image` (base URL `https://api-ssl.bitly.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code-image.md) for the provider-specific parameters and requirements.

