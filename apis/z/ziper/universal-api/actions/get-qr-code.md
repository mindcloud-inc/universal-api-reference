# Ziper: Get QR Code

Retrieves a WhatsApp login QR code from Ziper.

```
GET https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziper/latest/actions/get-qr-code?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "base64": "https://example.com",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base64` | string | Base64 data URL for the QR code image used to link the WhatsApp instance. |
| `message` | string | Provider result message. |
| `status` | string | Provider status returned by Ziper. |

## Native endpoint

Through the native Ziper API, this operation is `GET /getqrcode.php` (base URL `https://ziper.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.

