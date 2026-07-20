# ME-QR: Create WhatsApp QR

Creates a WhatsApp QR code in ME-QR.

```
POST https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/create-whats-app-qr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ME-QR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/create-whats-app-qr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrFieldsData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/create-whats-app-qr', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrFieldsData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrFieldsData` | object | yes | Provider-defined payload object for this QR type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "qrUrl": "https://example.com",
      "type": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `qrUrl` | string |  |
| `type` | number |  |
| `url` | string |  |

## Native endpoint

Through the native ME-QR API, this operation is `POST /api/v2/qr/whatsapp/create` (base URL `https://me-qr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-whats-app-qr.md) for the provider-specific parameters and requirements.

