# goQR.me Universal API Examples

These examples use the MindCloud API key and goQR.me connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Read QR Code

Reads a QR code with goQR.me.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/read-qr-code?${params}`, {
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
  "data": [
    {
      "symbol": [
        {
          "data": "string",
          "error": "string",
          "seq": 1
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Read QR Code action reference](actions/read-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goQRme/latest/actions/read-qr-code).

## Create QR Code

Creates a QR code with goQR.me.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/create-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "Hello World"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goQRme/latest/actions/create-qr-code', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "Hello World"
  })
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

See the full [Create QR Code action reference](actions/create-qr-code.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goQRme/latest/actions/create-qr-code).
