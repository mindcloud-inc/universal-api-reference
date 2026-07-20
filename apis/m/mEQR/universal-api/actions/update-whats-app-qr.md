# ME-QR: Update WhatsApp QR

Updates a WhatsApp QR code in ME-QR.

```
PUT https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/update-whats-app-qr
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ME-QR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/update-whats-app-qr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entryUID": "string",
  "qrFieldsData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/update-whats-app-qr', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entryUID": "string",
    "qrFieldsData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryUID` | string | yes | ID or unique entry key for the QR code. |
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

Through the native ME-QR API, this operation is `PUT /api/v2/qr/whatsapp/update/:entryUID` (base URL `https://me-qr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-whats-app-qr.md) for the provider-specific parameters and requirements.

