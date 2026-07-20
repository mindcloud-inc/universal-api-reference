# OpenQR: Update QR Code

Updates an existing QR code in OpenQR.

```
PUT https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenQR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrCodeId": "Ty5C1sug",
  "name": "Updated QR Code",
  "type": "url",
  "data": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openQR/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrCodeId": "Ty5C1sug",
    "name": "Updated QR Code",
    "type": "url",
    "data": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrCodeId` | string | yes | QR Code ID. Example: `Ty5C1sug`. |
| `name` | string | yes | QR code name. Example: `Updated QR Code`. |
| `type` | list | yes | QR code type. One of: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Example: `url`. |
| `data` | object | yes | Type-specific QR code data object. Example: `[object Object]`. |

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

Through the native OpenQR API, this operation is `POST /qr-codes/:qr_code_id` (base URL `https://api.openqr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.

