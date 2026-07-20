# Recut URL Shortener: Update QR Code

Updates an existing QR code in Recut URL Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "843",
  "data": "https://example.com/updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "843",
    "data": "https://example.com/updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | QR code ID Example: `843`. |
| `type` | list | no | text \| vcard \| link \| email \| phone \| sms \| wifi One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. Example: `link`. |
| `data` | string | yes | QR code data Example: `https://example.com/updated`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `background` | string | no | Background color Example: `#ffffff`. |
| `foreground` | string | no | Foreground color Example: `#000000`. |
| `logo` | string | no | Logo URL Example: `https://example.com/logo.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `PUT /qr/:id/update` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.

