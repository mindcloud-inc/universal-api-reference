# PayTabs Universal API Examples

These examples use the MindCloud API key and PayTabs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query Transaction by Reference



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference?connectionId=$CONNECTION_ID&tran_ref=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tran_ref": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/query-transaction-by-reference?${params}`, {
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
      "cartId": "string",
      "code": 1,
      "message": "string",
      "paymentResult": {},
      "profileId": 1,
      "trace": "string",
      "tranRef": "string"
    }
  ],
  "meta": {}
}
```

See the full [Query Transaction by Reference action reference](actions/query-transaction-by-reference.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payTabs/latest/actions/query-transaction-by-reference).

## Cancel Invoice



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/cancel-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/cancel-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice_id": "string"
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
      "code": 1,
      "invoiceId": "string",
      "invoiceStatus": "string",
      "message": "string",
      "trace": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Invoice action reference](actions/cancel-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payTabs/latest/actions/cancel-invoice).
