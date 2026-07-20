# OpenQR: Create Text QR Code

Creates a text QR code in OpenQR.

```
POST https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-text-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenQR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-text-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Demo QR Code",
  "data.text": "This is demo text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-text-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Demo QR Code",
    "data.text": "This is demo text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | QR code name. Example: `Demo QR Code`. |
| `data.text` | string | yes | Text to encode in the QR code. Example: `This is demo text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domainId": "string",
      "dynamic": true,
      "id": "string",
      "image": "https://example.com",
      "name": "Ava Chen",
      "qrCodeFolderId": 1,
      "status": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `domainId` | string |  |
| `dynamic` | boolean |  |
| `id` | string |  |
| `image` | string |  |
| `name` | string |  |
| `qrCodeFolderId` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native OpenQR API, this operation is `POST /qr-codes` (base URL `https://api.openqr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-text-qr-code.md) for the provider-specific parameters and requirements.

