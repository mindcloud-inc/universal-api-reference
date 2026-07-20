# edatalia Sign Online Universal API Examples

These examples use the MindCloud API key and edatalia Sign Online connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Devices

Retrieves available devices from edatalia Sign Online.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/list-devices?${params}`, {
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
      "alias": "string",
      "deviceId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Devices action reference](actions/list-devices.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edataliaSignOnline/latest/actions/list-devices).

## Sign PDF With Certificate

Signs a PDF with a certificate in edatalia Sign Online.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/sign-pdf-with-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "b64PDFContent": "string",
  "widget": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edataliaSignOnline/latest/actions/sign-pdf-with-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "b64PDFContent": "string",
    "widget": {}
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
      "content": "string"
    }
  ],
  "meta": {}
}
```

See the full [Sign PDF With Certificate action reference](actions/sign-pdf-with-certificate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/edataliaSignOnline/latest/actions/sign-pdf-with-certificate).
