# retailCRM Universal API Examples

These examples use the MindCloud API key and retailCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from retailCRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-users?${params}`, {
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
      "active": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {
          "code": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "id": 1,
      "isAdmin": true,
      "isManager": true,
      "lastName": "Chen",
      "online": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retailCRM/latest/actions/list-users).

## Create Customer

Creates a new customer in retailCRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "site": "string",
  "customer.externalId": "string",
  "customer.firstName": "Ava",
  "customer.phones[0].number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "site": "string",
    "customer.externalId": "string",
    "customer.firstName": "Ava",
    "customer.phones[0].number": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/retailCRM/latest/actions/create-customer).
