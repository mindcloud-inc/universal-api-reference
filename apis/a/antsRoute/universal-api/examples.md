# AntsRoute Universal API Examples

These examples use the MindCloud API key and AntsRoute connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Finds orders in AntsRoute by selected criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/list-orders?${params}`, {
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

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/antsRoute/latest/actions/list-orders).

## Create Customer

Creates a new customer in AntsRoute.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "string",
  "lastName": "Chen",
  "latitude": 1,
  "longitude": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "string",
    "lastName": "Chen",
    "latitude": 1,
    "longitude": 1
  })
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

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/antsRoute/latest/actions/create-customer).
