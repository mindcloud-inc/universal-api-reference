# InvoiceBerry Universal API Examples

These examples use the MindCloud API key and InvoiceBerry connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Currencies



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-currencies?${params}`, {
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
      "code": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Currencies action reference](actions/list-currencies.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiceBerry/latest/actions/list-currencies).

## Create Expense



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/create-expense', {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Expense action reference](actions/create-expense.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiceBerry/latest/actions/create-expense).
