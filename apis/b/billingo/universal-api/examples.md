# Billingo Universal API Examples

These examples use the MindCloud API key and Billingo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Server Time

Retrieves the current server time from Billingo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-server-time?${params}`, {
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
      "epoch": 1,
      "formatted": "string",
      "timezone": "string",
      "w3c": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Server Time action reference](actions/get-server-time.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billingo/latest/actions/get-server-time).

## Copy Document

Creates a copy of a document in Billingo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/copy-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billingo/latest/actions/copy-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "0"
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
      "currency": "string",
      "gross_total": 1,
      "id": 1,
      "invoice_number": "string",
      "payment_status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Copy Document action reference](actions/copy-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/billingo/latest/actions/copy-document).
