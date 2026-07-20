# Qryptal Universal API Examples

These examples use the MindCloud API key and Qryptal connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Download QR Code Image



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image?connectionId=$CONNECTION_ID&uid=1097580178100010000601672116&codeToken=C02%3ArFKsq1dyUmJZZFNze1Jr..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "1097580178100010000601672116",
  "codeToken": "C02:rFKsq1dyUmJZZFNze1Jr..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/download-qr-code-image?${params}`, {
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

See the full [Download QR Code Image action reference](actions/download-qr-code-image.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qryptal/latest/actions/download-qr-code-image).

## Generate EDC QR Code With Attachments



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/generate-edc-qr-code-with-attachments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payload": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qryptal/latest/actions/generate-edc-qr-code-with-attachments', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payload": "[object Object]"
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
      "apitype": "string",
      "codeToken": "string",
      "ct": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "msg": "string",
      "qrText": "string",
      "qrurl": "https://example.com",
      "scheme": "string",
      "status": "string",
      "uid": "string",
      "vqtype": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate EDC QR Code With Attachments action reference](actions/generate-edc-qr-code-with-attachments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/qryptal/latest/actions/generate-edc-qr-code-with-attachments).
