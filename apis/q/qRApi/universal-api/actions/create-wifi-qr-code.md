# QR Api: Create WiFi QR Code

Creates a QR code for Wi-Fi access in QR Api.

```
POST https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-wifi-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QR Api `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-wifi-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ssid": "Office WiFi"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-wifi-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ssid": "Office WiFi"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ssid` | string | yes | Exact WiFi network name to encode. Example: `Office WiFi`. |
| `authentication` | string | no | WiFi authentication type. Default: `WPA`. |
| `psk` | string | no | WiFi password or pre-shared key. |

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

Through the native QR Api API, this operation is `GET /qrcode/wifi` (base URL `https://qrapi.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wifi-qr-code.md) for the provider-specific parameters and requirements.

