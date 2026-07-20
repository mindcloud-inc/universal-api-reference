# KlipLink: Create QR Code



```
POST https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KlipLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationUrl` | string | yes | The destination URL the QR code should redirect to. |
| `title` | string | no | Optional title for the QR code. |
| `description` | string | no | Optional description for the QR code. |
| `domain` | string | no | Optional custom domain for the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accent_color": "string",
      "background_color": "string",
      "clicks": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_url": "https://example.com",
      "eye_style": "string",
      "shape": "string",
      "short_url": "https://example.com",
      "success": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accent_color` | string | Foreground hex color for the QR code. |
| `background_color` | string | Background hex color for the QR code. |
| `clicks` | number | Current click count for the QR code. |
| `created_at` | date | Creation timestamp for the QR code. |
| `destination_url` | string | Destination URL stored for the QR code. |
| `eye_style` | string | Style of the QR code eyes. |
| `shape` | string | Shape of the QR code modules. |
| `short_url` | string | Short URL created for the QR code. |
| `success` | boolean | Whether the request succeeded. |
| `title` | string | Title for the QR code. |

## Native endpoint

Through the native KlipLink API, this operation is `POST /v1/qrcodes` (base URL `https://api.klipl.ink`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.

