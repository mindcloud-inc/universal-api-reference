# PayWhirl Universal API Examples

These examples use the MindCloud API key and PayWhirl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection

Retrieves connection details from PayWhirl.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/test-connection?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payWhirl/latest/actions/test-connection).

## Add Promo To Invoice

Adds a promo code to a PayWhirl invoice.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/add-promo-to-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/add-promo-to-invoice', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Promo To Invoice action reference](actions/add-promo-to-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/payWhirl/latest/actions/add-promo-to-invoice).
