# QR Api Universal API Examples

These examples use the MindCloud API key and QR Api connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create Email QR Code

Creates a QR code for an email address in QR Api.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-email-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "hello@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qRApi/latest/actions/create-email-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "hello@example.com"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Email QR Code action reference](actions/create-email-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qRApi/latest/actions/create-email-qr-code).
