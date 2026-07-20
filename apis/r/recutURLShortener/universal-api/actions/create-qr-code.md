# Recut URL Shortener: Create QR Code

Creates a QR code in Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "link",
  "data": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "link",
    "data": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | yes | text \| vcard \| link \| email \| phone \| sms \| wifi One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Example: `link`. |
| `data` | string | yes | Data to be embedded inside the QR code Example: `https://example.com`. |
| `name` | string | no | QR Code name Example: `MindCloud QR`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background` | string | no | RGB color such as rgb(255,255,255) Example: `rgb(255,255,255)`. |
| `foreground` | string | no | RGB color such as rgb(0,0,0) Example: `rgb(0,0,0)`. |
| `logo` | string | no | Path to the logo either png or jpg Example: `https://site.com/logo.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "id": 1,
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number |  |
| `id` | number |  |
| `link` | string |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /qr/add` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-qr-code.md) for the provider-specific parameters and requirements.

