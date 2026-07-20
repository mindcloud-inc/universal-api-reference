# Engage Universal API Examples

These examples use the MindCloud API key and Engage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Engage with optional email filtering.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users?${params}`, {
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
      "accounts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isAccount": true,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "memberCount": 1,
      "meta": {},
      "number": "string",
      "segments": [
        {}
      ],
      "stats": {},
      "uid": "string",
      "uidUpdateable": true
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/engage/latest/actions/list-users).

## Add Customer to Accounts

Adds a customer to one or more accounts in Engage.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/engage/latest/actions/add-customer-to-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accounts[]": [
    {}
  ],
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/add-customer-to-accounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accounts[]": [{}],
    "uid": "string"
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
      "accounts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isAccount": true,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "memberCount": 1,
      "meta": {},
      "number": "string",
      "segments": [
        {}
      ],
      "stats": {},
      "uid": "string",
      "uidUpdateable": true
    }
  ],
  "meta": {}
}
```

See the full [Add Customer to Accounts action reference](actions/add-customer-to-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/engage/latest/actions/add-customer-to-accounts).
