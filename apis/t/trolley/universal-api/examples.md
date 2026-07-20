# Trolley Universal API Examples

These examples use the MindCloud API key and Trolley connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Recipients

Retrieves all recipient records from Trolley.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trolley/latest/actions/list-recipients?${params}`, {
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
      "meta": {},
      "ok": true,
      "recipients": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Recipients action reference](actions/list-recipients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trolley/latest/actions/list-recipients).

## Create Invoice

Creates a new invoice in Trolley.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trolley/latest/actions/create-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "invoice": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

See the full [Create Invoice action reference](actions/create-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/trolley/latest/actions/create-invoice).
