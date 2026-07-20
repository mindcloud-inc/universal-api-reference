# PrexView Universal API Examples

These examples use the MindCloud API key and PrexView connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create document from JSON

Creates a document in PrexView from JSON data.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "json": "Paste JSON data",
  "template": "invoice-customer-{{Data.customer}}",
  "output": "pdf"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prexView/latest/actions/create-document-from-json', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "json": "Paste JSON data",
    "template": "invoice-customer-{{Data.customer}}",
    "output": "pdf"
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
      "content": "string",
      "contentType": "string",
      "rateLimitLimit": 1,
      "rateLimitRemaining": 1,
      "rateLimitReset": 1,
      "transactionId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create document from JSON action reference](actions/create-document-from-json.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prexView/latest/actions/create-document-from-json).
