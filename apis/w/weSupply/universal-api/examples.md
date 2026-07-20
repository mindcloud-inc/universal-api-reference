# WeSupply Universal API Examples

These examples use the MindCloud API key and WeSupply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Customer Data

Retrieves customer data from WeSupply.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/get-customer-data?${params}`, {
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
      "CustomerEmail": "ava@example.com",
      "OrderContact": "string",
      "OrderExternalOrderID": "string",
      "OrderNumber": "string",
      "OrderShippingPhone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Customer Data action reference](actions/get-customer-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weSupply/latest/actions/get-customer-data).

## Approve Return

Approves an existing return in WeSupply.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/approve-return" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weSupply/latest/actions/approve-return', {
  method: 'PUT',
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Approve Return action reference](actions/approve-return.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weSupply/latest/actions/approve-return).
