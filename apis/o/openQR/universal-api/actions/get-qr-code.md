# OpenQR: Get QR Code

Retrieves a QR code from the OpenQR account.

```
GET https://connect.mindcloud.co/v1/universal/openQR/latest/actions/get-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenQR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/get-qr-code?connectionId=$CONNECTION_ID&qrCodeId=Ty5C1sug" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCodeId": "Ty5C1sug"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openQR/latest/actions/get-qr-code?${params}`, {
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
| `qrCodeId` | string | yes | QR Code ID. Example: `Ty5C1sug`. |

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

Through the native OpenQR API, this operation is `GET /qr-codes/:qr_code_id` (base URL `https://api.openqr.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-qr-code.md) for the provider-specific parameters and requirements.

