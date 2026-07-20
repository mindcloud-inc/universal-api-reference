# QR Api: Create SMS QR Code

Creates a QR code for a prefilled SMS in QR Api.

```
POST https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-sms-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QR Api `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-sms-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNo": "+14155550123",
  "message": "Your message"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-sms-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNo": "+14155550123",
    "message": "Your message"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phoneNo` | string | yes | Recipient phone number for the SMS QR code. Example: `+14155550123`. |
| `message` | string | yes | SMS message to encode in the QR code. Example: `Your message`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `size` | string | no | QR code size preset: s, m, l, xl, xxl, xxxl, or custom. Default: `m`. |
| `format` | string | no | QR code output format: png, jpg, svg, pdf, or eps. Default: `png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | PNG image bytes for the generated QR code. |
| `type` | string | Node buffer marker for the generated QR code image. |

## Native endpoint

Through the native QR Api API, this operation is `GET /qrcode/SMS` (base URL `https://qrapi.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sms-qr-code.md) for the provider-specific parameters and requirements.

