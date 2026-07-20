# Uniqode: Delete QR Code

Deletes an existing QR code from Uniqode.

```
DELETE https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/delete-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uniqode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/delete-qr-code?connectionId=$CONNECTION_ID&qrCodeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "qrCodeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uniqode/latest/actions/delete-qr-code?${params}`, {
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
| `qrCodeId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Uniqode API returns.

## Native endpoint

Through the native Uniqode API, this operation is `DELETE /qrcodes/:qrCodeId/` (base URL `https://api.uniqode.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-qr-code.md) for the provider-specific parameters and requirements.

