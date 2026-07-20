# Zahara Universal API Examples

These examples use the MindCloud API key and Zahara connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users (Business Unit)

Retrieves users from a Zahara business unit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zahara/latest/actions/list-users-business-unit?${params}`, {
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
      "Email": "ava@example.com",
      "FirstName": "Ava",
      "JobTitle": "string",
      "LastName": "Chen",
      "UserId": 1,
      "UserName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users (Business Unit) action reference](actions/list-users-business-unit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zahara/latest/actions/list-users-business-unit).

## Create Invoice

Creates a new invoice in Zahara.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zahara/latest/actions/create-invoice', {
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
      "DocumentId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Invoice action reference](actions/create-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zahara/latest/actions/create-invoice).
