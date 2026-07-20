# TLY Link Shortener: Update QR Code

Updates a QR code in TLY Link Shortener.

```
PUT https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shortUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shortUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shortUrl` | string | yes | The short URL whose QR code should be updated. |
| `image` | string | no | Optional QR code image as a base64 data URL. |
| `backgroundColor` | string | no | Optional background color for the QR code. |
| `cornerDotsColor` | string | no | Optional corner dots color for the QR code. |
| `dotsColor` | string | no | Optional dots color for the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "qr_code_options": {},
      "short_url": "https://example.com",
      "team_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `qr_code_options` | object |  |
| `short_url` | string |  |
| `team_id` | number |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `PUT /api/v1/link/qr-code` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.

