# ME-QR Universal API Examples

These examples use the MindCloud API key and ME-QR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List QRs

Retrieves all QR codes from ME-QR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/list-q-rs?${params}`, {
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
      "currentPageNumber": 1,
      "items": [
        {}
      ],
      "lastPageNumber": 1,
      "numItemsPerPage": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List QRs action reference](actions/list-q-rs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mEQR/latest/actions/list-q-rs).

## Create Email QR

Creates an email QR code in ME-QR.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/create-email-qr" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrFieldsData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mEQR/latest/actions/create-email-qr', {
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

Example response:

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

See the full [Create Email QR action reference](actions/create-email-qr.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mEQR/latest/actions/create-email-qr).
