# OpenQR Universal API Examples

These examples use the MindCloud API key and OpenQR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Lists QR logo files in the OpenQR account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/list-files?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openQR/latest/actions/list-files?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openQR/latest/actions/list-files).

## Create Call QR Code

Creates a call QR code in OpenQR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-call-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Demo QR Code",
  "data.phone": "+1234567890"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openQR/latest/actions/create-call-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Demo QR Code",
    "data.phone": "+1234567890"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Call QR Code action reference](actions/create-call-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/openQR/latest/actions/create-call-qr-code).
