# Salebot Universal API Examples

These examples use the MindCloud API key and Salebot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/list-clients?${params}`, {
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
      "clients": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salebot/latest/actions/list-clients).

## Create Order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salebot/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1
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
      "orderId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salebot/latest/actions/create-order).
