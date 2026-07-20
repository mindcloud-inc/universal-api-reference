# CodeQR - Link and QR Analytics: Upsert QR Code

Updates or creates a QR code in CodeQR.

```
PUT https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/upsert-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/upsert-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/upsert-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | The type of content of the QR code. |
| `url` | string | no | The destination URL of the QR code. |
| `title` | string | no | The title of the QR code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "externalId": "string",
      "id": "string",
      "image": "string",
      "key": "string",
      "scans": 1,
      "shortLink": "https://example.com",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `domain` | string |  |
| `externalId` | string |  |
| `id` | string |  |
| `image` | string |  |
| `key` | string |  |
| `scans` | number |  |
| `shortLink` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `PATCH /qrcodes/upsert` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-qr-code.md) for the provider-specific parameters and requirements.

