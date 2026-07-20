# CodeQR - Link and QR Analytics: Delete QR Code

Deletes a QR code from CodeQR.

```
DELETE https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-qr-code?connectionId=$CONNECTION_ID&qrcodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrcodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/delete-qr-code?${params}`, {
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
| `qrcodeId` | string | yes | The ID of the QR code to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `DELETE /qrcodes/:qrcodeId` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-qr-code.md) for the provider-specific parameters and requirements.

