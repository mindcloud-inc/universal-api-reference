# goQR.me: Create QR Code

Creates a QR code with goQR.me.

```
POST https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a goQR.me `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "Hello World"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "Hello World"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes | Text to encode in the QR code. Example: `Hello World`. |
| `size` | string | no | Generated QR code size in pixels. Default: `200x200`. Example: `200x200`. |
| `charsetSource` | list<string> | no | Charset used to encode the input text. One of: `ISO-8859-1`, `UTF-8`. Default: `UTF-8`. |
| `charsetTarget` | list<string> | no | Charset to store inside the QR code. One of: `ISO-8859-1`, `UTF-8`. Default: `UTF-8`. |
| `ecc` | list<string> | no | QR error correction level. One of: `H`, `L`, `M`, `Q`. Default: `L`. |
| `color` | string | no | QR data-module color. Default: `0-0-0`. Example: `0-0-0`. |
| `bgcolor` | string | no | QR background color. Default: `255-255-255`. Example: `255-255-255`. |
| `margin` | number | no | Pixel margin around the QR code. Default: `1`. |
| `qzone` | number | no | Quiet zone around the QR code. Default: `0`. |
| `format` | list<string> | no | File format for the generated QR code image. One of: `eps`, `gif`, `jpeg`, `jpg`, `png`, `svg`. Default: `png`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native goQR.me API returns.

## Native endpoint

Through the native goQR.me API, this operation is `GET /create-qr-code/` (base URL `https://api.qrserver.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.

