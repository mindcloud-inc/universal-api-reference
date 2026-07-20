# OrderOut Universal API Examples

These examples use the MindCloud API key and OrderOut connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Restaurants

Lists restaurants in OrderOut.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/list-restaurants?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/list-restaurants?${params}`, {
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

See the full [List Restaurants action reference](actions/list-restaurants.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderOut/latest/actions/list-restaurants).

## Create Account

Creates an account in OrderOut.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountManagerEmail": "ava@example.com",
  "accountManagerFirstname": "Ava",
  "accountManagerLastname": "Chen",
  "accountManagerPhone": "string",
  "accountName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orderOut/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountManagerEmail": "ava@example.com",
    "accountManagerFirstname": "Ava",
    "accountManagerLastname": "Chen",
    "accountManagerPhone": "string",
    "accountName": "Ava Chen"
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
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orderOut/latest/actions/create-account).
