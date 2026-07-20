# Geral: Get QR Code

Retrieves a QR code from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&qrCodeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCodeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-qr-code?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrCodeId` | number | yes | The QR code ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "embedded_data": "string",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "qr_code": "https://example.com",
      "qr_code_background": "https://example.com",
      "qr_code_logo": "https://example.com",
      "settings": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date | Creation timestamp. |
| `embedded_data` | string | Data embedded in the QR code. |
| `id` | number | QR code ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | QR code name. |
| `qr_code` | string | QR code image URL. |
| `qr_code_background` | string | QR code background URL. |
| `qr_code_logo` | string | QR code logo URL. |
| `settings` | object | QR code settings. |
| `type` | string | QR code type. |

## Native endpoint

Through the native Geral API, this operation is `GET /qr-codes/:qr_code_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.

